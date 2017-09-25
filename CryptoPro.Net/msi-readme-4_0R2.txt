Ниже приведены доступные параметры для Windows Installer:

Следующие опции позволяют не устанавливать соответствующие библиотеки поддержки:
NOACCORD=1	- Аккорд
NOBIO=1		- Биологический ДСЧ
NODALLAS=1	- Носители Dallas
NODS=1		- Считыватели Dallas
NODSRF=1	- ДСЧ "Последовательность поставщика"
NOEMV=1		- Карта EMV
NOETOKEN=1	- Носители eToken
NOFLOPPY=1	- Считыватель дискет
NOJCARD=1	- Карты JCard
NOPCSC=1	- PC/SC
NOREGISTRY=1	- Считыватель "Реестр"
NORIC=1		- Карты RIC/OSCAR
NORUTOKEN=1	- Носители Rutoken
NOSABLE=1	- Соболь
NOSNET=1	- SecretNet
NOCHARISMATHICS - Charismathics
NOINPAS		- Global Platform Optelio

Следующие опции позволяют управлять регистрацией поддерживаемого оборудования:
(значение 0 означает "не регистрировать" для тех, что регистрируются по умолчанию*)

REGACCORDRDR=1		- Зарегистрировать считыватель "Аккорд" во время установки
REGACCORDRND=1		- Зарегистрировать ДСЧ "Аккорд" во время установки
REGAPMDZRND=1		- Зарегистрировать ДСЧ "Анкад" во время установки
REGBIO=1		- Зарегистрировать биологический ДСЧ *(только для КС1)
REGCHARISMATHICS=1	- Зарегистрировать все носители "Charismathics" во время установки
REGESMARTTOKEN=1	- Зарегистрировать носители "ESMARTToken" во время установки
REGESMARTTOKENGOST=1 - Зарегистрировать носители "ESMARTTokenGost" во время установки
REGESMARTTOKENBIO=1	- Включить биометрическую аутентификацию для "ESMARTToken" во время установки
REGETOKEN=1		- Зарегистрировать все носители "Aladdin eToken", отдельные типы: REGETOKENJAVA10, REGETOKENJAVA10B, REGETOKENM420, REGETOKENM420B, REGETOKEN16, REGETOKEN32, REGETOKENR2
REGGTOKEN=1		- Зарегистрировать все носители "eToken GOST"
REGFLOPPY=буквы		- Зарегистрировать считыватель "дискета" (FAT12/FLOPPY) для букв, указанных через запятую
REGPNPFLOPPY=1		- Зарегистрировать считыватель "Все съемные носители" *
REGDSRF=путь		- Зарегистрировать ДСЧ "Последовательность поставщика" и задать путь (без "\" на конце) к папке с db1, db2
REGDS1410E=порты	- Зарегистрировать считыватель "DS1410E" (порты - список портов через запятую: LPT1,LPT2,...)
REGDS9097E=порты	- Зарегистрировать считыватель "DS9097E" (порты - список портов через запятую: COM1,COM2,...)
REGDS9097U=порты	- Зарегистрировать считыватель "DS9097U" (порты - список портов через запятую: COM1,COM2,...)
REGDS199X=1		- Зарегистрировать носитель "DS199x"
REGEMV=1		- Зарегистрировать носитель "MPCOS EMV"
REGGEMALTO=1		- Зарегистрировать носитель "GEMALTO"
REGINPAS=1		- Зарегистрировать носители "ИНПАС"
REGISBC=1		- Зарегистрировать носители "ISBC"
REGKST=1		- Зарегистрировать носители "KST"
REGMSKEY=1		- Зарегистрировать носители "MSKEY"
REGNOVACARD=1		- Зарегистрировать носители "NOVACARD"
REGISBC=1		- Зарегистрировать носители "ISBC"
REGOSCAR=1		- Зарегистрировать носитель "Оскар"
REGOSCAR2=1		- Зарегистрировать носитель "Оскар2" *
REGTRUST=1		- Зарегистрировать носитель "Магистра" *
REGTRUSTS=1		- Зарегистрировать носитель "Магистра Сбербанк/BGS" *
REGTRUSTD=1		- Зарегистрировать носитель "Магистра Debug" *
REGPNPPCSC=1		- Зарегистрировать считыватель "Все считыватели смарт-карт" *
REGREGISTRY=1		- Зарегистрировать считыватель "Реестр"
REGRIC=1		- Зарегистрировать носитель "РИК"
REGRUTOKEN=1		- Зарегистрировать носитель "Rutoken" *
REGSABLERDR=1		- Зарегистрировать считыватель "Соболь"
REGSABLERND=1		- Зарегистрировать ДСЧ "Соболь"

NOWL=1			- Не регистрировать носители для Winlogon

Не регистрировать носители для Winlogon:
NOESMARTTOKENWL=1	- "ESMARTTOKEN"
NOETOKENWL=1		- "Aladdin eToken"
NOGEMALTOWL=1		- "GEMALTO"
NOISBCWL=1		- "ISBC"
NOGKSTWL=1		- "KST"
NOGMSKEYWL=1		- "MSKEY"
NOGNOVACARDWL=1		- "NOVACARD"
NOOSCAR2WL=1		- "Оскар2"
NOTRUSTWL=1		- "Магистра"
NOTRUSTSWL=1		- "Магистра Сбербанк/BGS"
NOTRUSTDWL=1		- "Магистра Debug"
NORUTOKENWL=1		- "Rutoken"
NOCHARISMATHICSWL=1	- "Charismathics"
NOINPASWL=1		- "ИНПАС"

Другие:
NODIAGTRACKDISABLE=1 - не отключать шпионские функции Windows
NOINTERACTIVESERVICES=1 - позволяет не разрешать интерактивные сервисы Windows, отключенные по умолчанию на Windows 8
CPCSPR=1	- Для версии KC1 позволяет выбрать режим службы хранения ключей (только при установке)
MEDIACSPS=1	- Использовать "носительные" провайдеры (только при установке)
CACHED=N	- Настройка кэширования ключей. Если N=0, то выключено, если N>0, то задает размер кэша (только при установке)
CSPDELETEKEYS=1	- При удалении продукта удалит так же все настройки и все ключи из реестра
INSTALLCPCERT=1	- Установить сертификат подписи кода КРИПТО-ПРО в хранилище "Доверенные издатели" (позволяет избежать запрос на установку драйвера на Windows 6+)
DISABLE_SHORTCUTS=1 - Не сохранять информацию об использованных съемных носителях
CERTSTOREPARAMSSUPPORTED=1 Включить поддержку параметров PP_USER_CERTSTORE/PP_ROOT_CERTSTORE
FULLCNGREGISTER=1 Зарегистрировать Key Storage Provider (CNG)
LICERRORLEVEL=[1][2][4] - Битовая маска отлючения отображения ошибок лицензии
  001 IDS_CSP_CORRUPTED 
  010 IDS_CSP_EXPIRED, IDS_WRONG_LICENSE_TYPE, IDS_CSP_EXPIRED_CERT_BAD
  100 IDS_CSP_EXPIRE_IN...
ENABLEDEFAULTREADER=1 Разрешить использовать считыватель по умолчанию

Устанавливаемые компоненты:
REPROV=1	- Установить компоненту "Revocation Provider"
DRIVER=1	- Установить компоненту "Драйверная библиотека CSP"
COMPAT=1	- Установить компоненту "Совместимость с КриптоПро CSP 3.0"
NODRIVER=1	- Не устанавливать компоненту "Драйверная библиотека CSP" (ставится по умолчанию на Windows Server 2008)
NOCPROCTRL=1	- Не устанавливать компоненту "Совместимость с продуктами Microsoft" (ставится по умолчанию)
NOCCID=1 - Не устанавливать драйвер CCID (Chip/Smart Card Interface Devices) 

Ввод серийных номеров:
COMPANYNAME=    - Указать название организации, использующей лицензию
USERNAME=       - Указать имя пользователя, использующего лицензию
PIDKEY=		- Использовать указанный серийный номер CSP
WLPIDKEY=	- Использовать указанный серийный номер Winlogon
RPPIDKEY=	- Использовать указанный серийный номер Revocation Provider
OCSPAPIPIDKEY=  - Использовать указанный серийный номер OCSP Client
TSPAPIPIDKEY=   - Использовать указанный серийный номер TSP Client

Встроенные в Windows Installer:
PATCH=патчи	- Установить продукт вместе с патчами (список полный путей к .msp-файлам через точку с запятой)
INSTALLDIR=...	- Путь установки
INSTALLDIR64=...- Путь установки для 64-компонент
REBOOT=R	- Не перезагружать компьютер после установки
REMOVE=модули   - ДЛЯ УЖЕ УСТАНОВЛЕННОГО ПРОДУКТА удаляет указанные модули (cproctrl, reprov, driver, compat)
ADDLOCAL=модули - ДЛЯ УЖЕ УСТАНОВЛЕННОГО ПРОДУКТА устанавливает указанные модули (cproctrl, reprov, driver, compat)

/qb 		- установка без мастера
/qn 		- установка без окон
/L*v файл	- создание журнала установки

Для удаления CSP: msiexec /x {407E5BA7-6406-40BF-A4DC-3654B8F584C1}
