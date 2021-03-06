# start with this container as the base
FROM microsoft/windowsservercore

LABEL Description="RabbitMQ" Vendor="Pivotal" Version="3.6.12"

    # erlang installer download url
ENV erlang_download_url="http://erlang.org/download/otp_win64_20.0.exe" \
    # erlang will install to this location and rabbitmq will use this environment variable to locate it
    ERLANG_HOME=c:\\erlang \
    # rabbitmq version used in download url and to rename folder extracted from zip file
    rabbitmq_version="3.6.12" \
    # tell rabbitmq where to find our custom config file
    RABBITMQ_CONFIG_FILE="c:\rabbitmq"

# rabbitmq zip package download url
ENV rabbit_download_url "https://www.rabbitmq.com/releases/rabbitmq-server/v$rabbitmq_version/rabbitmq-server-windows-$rabbitmq_version.zip"

# setup powershell options for RUN commands
SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]

EXPOSE 5672 15672

# download and install erlang using silent install option, and remove installer when done
RUN Invoke-WebRequest -Uri $env:erlang_download_url -OutFile erlang_install.exe ; \
        Start-Process -Wait -FilePath .\erlang_install.exe -ArgumentList /S, /D=$env:ERLANG_HOME ; \
        Remove-Item -Force erlang_install.exe

# download and extract rabbitmq, and remove zip file when done
RUN Invoke-WebRequest -Uri $env:rabbit_download_url -OutFile rabbitmq.zip ; \
        Expand-Archive -Path .\rabbitmq.zip -DestinationPath "c:\\" ; \
        Remove-Item -Force rabbitmq.zip

# remove version from rabbitmq folder name
RUN Rename-Item c:\rabbitmq_server-$env:rabbitmq_version c:\rabbitmq

# enable managment plugin
RUN c:\rabbitmq\sbin\rabbitmq-plugins.bat enable rabbitmq_management --offline

# create config file
RUN ["cmd", "/c", "echo [{rabbit, [{loopback_users, []}]}].> c:\\rabbitmq.config"]

# run server when container starts - container will shutdown when this process ends
CMD "c:\rabbitmq\sbin\rabbitmq-server.bat"