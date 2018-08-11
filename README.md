## KoobAudio-dictionary
Русский словарь для приложения KoobAudio - программы для преобразования текста в аудиокниги или их прослушивания непосредственно из программы.
### Установка словаря
Данные словаря придназначены для обработки текста голосовым движком Digalo Nikolai 5.1 в программе KoobAudio, последнюю версию которой вы можете скачать по адресу http://koobaudio.narod.ru.
На данный момент на сайте выложена версия 2.1.2.8744 (05.02.2017), которая является самой рабочей и стабильной.
Сама программа KoobAudio предназначена для работы в операционных системах: Windows XP / Windows Vista / Windows 7 / Windows 8 (поддерживаются 32 и 64 битные версии ОС).

### Требования к операционной системе:

 - Процессор с тактовой частотой 1 ГГц или выше, рекомендуется 2+ ядерный процессор
 - Оперативная память: 256 МБ (XP) / 1024МБ (Vista / 7 / 8)
 - Разрешение экрана 1024x768 или выше
 - Microsoft .NET Framework 4.0
 - Microsoft Visual C++ 2010 Redistributable Package (x86)
 - SAPI5 совместимый и рекомендуемый речевой синтезатор «ELAN TTS Russian (Nicolai 16Khz)»
 
В случае запуска программы  KoobAudio в WINE, должны быть установлены следующие компоненты:
- dotnet40
- vcrun2010
- speechsdk
 
 ### Особенности установки самой программы:

На сайте программа KoobAudio доступна как в виде:
- portable-версии (без установки) http://koobaudio.narod.ru/files/koobaudio_2.1.2.8744.zip (рекомендуемая мною версия).
- в виде установочного файла http://koobaudio.narod.ru/files/koobaudio_2.1.2.8744_install.zip.

Данные словари должны быть установлены в папку Dic, которая присутсвует в данной программе по двум разным путям, в зависимотсти от того, какая программа у васустанволена (установочная версия или версия portable).

### Места располажения словарей KoobAudio
В случае установки запуска устоновочного файла файлы словарей будут располагаться в местах, которые зависят от  в зависимости  от версии вашей ОС.
При первом запуске программы будет предложен выбор папки, в которой будут сохраняться настройки и прочие файлы пользователя.

В однопользовательском режиме используется каталог Application Data текущего пользователя Windows. Т.е. у каждой учетной записи Windows будут свои настройки, книги в библиотеке и словари ударений.
Расположение каталога зависит от версии ОС:
-  Windows XP:		C:\Documents and Settings\Имя пользователя\Application Data\KooBAudio\
-  Windows Vista / Windows 7 /  Windows 8 /  Windows 10:	С:\Users\Имя пользователя\AppData\Roaming\KooBAudio\

В многопользовательском режиме используется каталог общий Application Data . Т.е. у всех учетных записей Windows будут общие настройки, книги в библиотеке и т.д.

Расположение каталога зависит от версии ОС:
- Windows XP:	C:\Documents and Settings\All Users\Application Data\KooBAudio\
- Windows Vista / Windows 7 /  Windows 8 /  Windows 10:			С:\ProgramData\KooBAudio\

 В portable режиме используется каталог, в котором расположен исполняемый файл программы. Настройки, книги в библиотеке и прочие данные не будут зависеть от учетной записи Windows. Папку с portable версией программы можно записать на любой внешний носитель и запускать на разных компьютерах (при условии, что на них установлен .NET Framework и нужный голосовой движок).

Не рекомендуется выбирать portable режим на операционных системах Windows Vista / 7, если программа была установлена в каталог Program Files, т.к. доступ к записи/изменению файлов в этой папке может быть заблокирован службой Windows UAC

### Установка словарей в системе
