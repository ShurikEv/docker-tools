# escape=`

# start with this container as the base
FROM microsoft/windowsservercore

LABEL Description="CryptoPro" Vendor="Bacup IT" Version="3.9R2"

# setup powershell options for RUN commands
SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]

#EXPOSE 1433
#WORKDIR Distr

#1. Ставим КриптоПро CSP

#RUN Write-Host 'Copy CryptoPro.msi' ; `
	#$MsiFile = 'csp-3_9R2-x64-kc2-eng.msi' ; ` 	
    #Copy-Item $MsiFile '\'; `
    #Write-Host 'Installing' ; 
    #Start-Process msiexec.exe -ArgumentList '/i', $MsiFile, '/qn', '/norestart', '/L*v', 'install.log' -NoNewWindow -Wait `
	#Remove-Item -Force $MsiFile
COPY ["csp-3_9R2-x64-kc2-eng.msi","/"]
#start /wait msiexec /i csp-3_9R2-x64-kc2-eng.msi /qn /norestart /L*v log/installCSP.log
#COPY ["install.bat","/"]
#RUN ["msiexec.exe", "/i", "csp-3_9R2-x64-kc2-eng.msi", "/qn", "/norestart", "/L*v", "installCSP.log"]
#RUN ["install.bat"]

#2. Ставим КриптоПро.NET
#RUN Write-Host 'Copy CryptoProNet.msi' ; `
#	$MsiFile = 'netsdk-x64-eng.msi' ; ` 
#    Copy-Item $MsiFile '\'; `
#    Write-Host 'Installing CryptoProNet' ; `
#    Start-Process msiexec.exe -ArgumentList '/i', $MsiFile, '/qn', '/norestart', '/L*v', 'install.log' -NoNewWindow -Wait `
#	Remove-Item -Force $MsiFile
COPY ["net-x64-eng.msi","/"] 
#RUN ["msiexec.exe", "/i", "net-x64-eng.msi", "/qn", "/norestart", "/L*v", "installNet.log"] > 
#start /wait msiexec /i net-x64-eng.msi /qn /norestart /L*v log/installNet.log

#3. Устанавливаем сертификаты ЭП-ОВ
#3.1 Ставим эмультор дискеты

# run server when container starts - container will shutdown when this process ends
COPY ["Start.ps1","/"]
CMD ./Start.ps1