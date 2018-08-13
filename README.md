## KoobAudio-dictionary
Русский словарь для приложения KoobAudio - программы для преобразования текста в аудиокниги или их прослушивания непосредственно из программы. Словари предназначены для обработки текста речевым синтезатором «ELAN TTS Russian (Nicolai 16Khz)».

Данный словарь придназначен для обработки текста голосовым движком Digalo Nikolai 5.1 в программе KoobAudio, последнюю версию которой вы можете скачать по адресу [koobaudio.narod.ru](http://koobaudio.narod.ru).
На данный момент на сайте выложена версия 2.1.2.8744 (05.02.2017), которая является самой рабочей и стабильной.
Сама программа KoobAudio предназначена для работы в операционных системах: Windows XP / Windows Vista / Windows 7 / Windows 8 (поддерживаются 32 и 64 битные версии ОС).

Словарь изначально заточен под работу в программме KoobAudio, которая имеет ряд особенностей (о чём ниже), но в принципе может быть использован и в других приложениях.

### Требования к операционной системе:
 - Процессор с тактовой частотой 1 ГГц или выше, рекомендуется 2+ ядерный процессор
 - Оперативная память: 256 МБ (XP) / 1024МБ (Vista / 7 / 8)
 - Разрешение экрана 1024x768 или выше
 - Microsoft .NET Framework 4.0
 - Microsoft Visual C++ 2010 Redistributable Package (x86)
 - SAPI5 совместимый и рекомендуемый речевой синтезатор «ELAN TTS Russian (Nicolai 16Khz)»
 
Для запуска программы  KoobAudio в WINE, должны быть установлены следующие компоненты:
 - mfc42
 - richtx32
 - riched30
 - vcrun2010
 - speechsdk
 - vcrun6
 - dotnet40

После установки компонентов, дополнительно устанавливаются Elan Tempo Multimedia.msi, koobaudio_2.1.2.8744. После установки, в настройках Spech выставляется язык SAPI DeveloperSample Engine.

 ### Особенности установки программы KoobAudio:
На сайте программа KoobAudio доступна:
 - в виде [portable-версии (без установки)](http://koobaudio.narod.ru/files/koobaudio_2.1.2.8744.zip) - рекомендуемая мною версия.
 - в виде [установочного файла](http://koobaudio.narod.ru/files/koobaudio_2.1.2.8744_install.zip).

Данные словари должны быть установлены в папку Dic, которая присутствует в данной программе по двум разным путям, в зависимости от того, какая программа у вас установлена (установочная версия или версия portable).

### Места расположения словарей KoobAudio
В случае установки запуска установочного файла, файлы словарей будут располагаться в местах, которые зависят от версии вашей ОС.
При первом запуске программы будет предложен выбор папки, в которой будут сохраняться настройки и прочие файлы пользователя.

В многопользовательском режиме используется каталог Application Data текущего пользователя Windows. Т.е. у каждой учетной записи Windows будут свои настройки, книги в библиотеке и словари ударений.
Расположение каталога:
 -  Windows XP:		C:\Documents and Settings\Имя пользователя\Application Data\KooBAudio\
 -  Windows Vista / Windows 7 /  Windows 8 /  Windows 10:	С:\Users\Имя пользователя\AppData\Roaming\KooBAudio\

В однопользовательском режиме используется каталог общий Application Data . Т.е. у всех учетных записей Windows будут общие настройки, книги в библиотеке и т.д.
Расположение каталога:
 - Windows XP:	C:\Documents and Settings\All Users\Application Data\KooBAudio\
 - Windows Vista / Windows 7 /  Windows 8 /  Windows 10:			С:\ProgramData\KooBAudio\

 В portable режиме используется каталог, в котором расположен исполняемый файл программы. Настройки, книги в библиотеке и прочие данные не будут зависеть от учетной записи Windows. Папку с portable версией программы можно записать на любой внешний носитель и запускать на разных компьютерах (при условии, что на них установлен .NET Framework и нужный голосовой движок).

Не рекомендуется выбирать portable режим на операционных системах Windows Windows Vista / Windows 7, если программа была установлена в каталог Program Files, т.к. доступ к записи/изменению файлов в этой папке может быть заблокирован службой Windows UAC.

### Установка словарей в portable-версии программы KoobAudio 
Если устанавливается portable-версия, то структура папок внутри программы иммет вид (c:\\Program Files\koobaudio_2.1.2.8744\):
  - Dic (подлежит удалению во избежание накладок при обработке текста)
  - enc
  - Portable\Dic (в данной папке размещаются словари)
1. Перейти в папку koobaudio_2.1.2.8744 и удалить папку Dic.
2. Далее, перейти в папку Portable\Dic и удалить из папки Dic все находящиеся в ней файлы.
3. Скопировать словари в данную папку. 

### Установка словарей в установочной версии программы KoobAudio
В зависимости от того какой вариант программы выбран, однопользовательский или многопользовательский:
1. перейти в папку пользователя:
  - C:\Documents and Settings\Имя пользователя\Application Data\KooBAudio\Dic
  - С:\Users\Имя пользователя\AppData\Roaming\KooBAudio\Dic
  - C:\ProgramData\KooBAudio\Dic
  - C:\Documents and Settings\All Users\Application Data\KooBAudio\Dic
  - С:\ProgramData\KooBAudio\Dic
 2. Удалить из папки Dic все находящиеся в ней файлы.
 3. Скопировать словари в данную папку. 
 
 ## Особенности обработки текста программой KoobAudio
 #### Принципы обработки текста правилами
 Словарь состоят из отдельных словарей-правил (далее под "словарём" будут подразумеваться только отдельные словари - правила), разделённых по тематике или каким-либо принципам, и имеющих чёткую структуру обработки текста. Такое разделение упрощает составление правил и уменьшает количество двойных ошибок при обработке текста (когда слово обрабатывается схожими правилами два и более раз).
 В словарях записаны правила идущие по порядку сверху-вниз. Программа "пропускает" каждое слово (символ) через правила, указанные в словарях, по порядку расположения правил в словаре, и вносит изменения в проверяемое слово (символ), если таковое имеется.
 
 После окончания проверки слова первым словарём, программа продолжает проверку вторым словарём, третьим и т.д. Поэтому все словари имеют в начале названия порядковый номер, означающий порядок обработки правилами.
 
 Программа, поддерживает два вида ударения в тексте: быстрое или скользящее ударение (символ >) и обычное ударение (символ <). Ударение ставится в слове после ударяемого гласного.
 
 Если в процесссе обработки слова в правилах будет найдено совпадение, в проверяемое слово вносится изменение - после гласной ставятся символы ъ<. Установка "ъ" улучшает произношение ударяемого гласного и предотвращает дальнейшую обработку проверяемого слова последующими правилами.
 
 Возможно так же изменение написания слова (словосочетания):
 
  - было: "кому-нибудь", стало: "комуъ<нибудь".
  - было: "Артек", стало: "Артэъ<к"
  
  Это делается с целью более комфортного произношения движком этого слова (словосочетания).
 
 Правила оформляются как в виде обычных текстовых уравнений, так и в виде регулярных выражений (Perl-совместимые регулярные выражения PCRE). Об особенностях регулярных выражений можно почитать [по ссылке](https://ru.wikipedia.org/wiki/Регулярные_выражения). Правила записанные регулярными выражениями предваряются символом #.
 
 Поддерживаются следующие типы правил упрощенного синтаксиса:
 
<table style="height: 304px; width: 525px;" border="1">
<tbody>
<tr style="height: 40px;">
<td style="width: 301px; text-align: center; height: 40px;">
<p><strong>Правила без учёта регистра&nbsp;</strong><strong>(кроме последнего)</strong></p>
</td>
<td style="width: 221px; text-align: center; height: 40px;" colspan="4"><strong>Соответствие в строке (подчеркнуто)</strong></td>
</tr>
<tr style="height: 40px;">
<td style="width: 301px; text-align: left; height: 40px;"><strong>&nbsp;Простые правила для отдельного слова:</strong><br />&nbsp;кот=КОТ</td>
<td style="width: 55px; text-align: center; height: 40px;"><u>КОТ</u></td>
<td style="width: 55px; text-align: center; height: 40px;">котел</td>
<td style="width: 55.48px; text-align: center; height: 40px;">скот</td>
<td style="width: 55.52px; text-align: center; height: 40px;">скотч.</td>
</tr>
<tr style="height: 40px;">
<td style="width: 301px; text-align: left; height: 40px;"><strong><span lang="EN-US">&nbsp;С</span><span class="SpellE">лово</span>&nbsp;целиком, или начало слова:</strong><br />&nbsp;кот*=КОТ</td>
<td style="width: 55px; text-align: center; height: 40px;"><span style="text-decoration: underline;">КОТ</span></td>
<td style="width: 55px; text-align: center; height: 40px;"><span style="text-decoration: underline;">КОТ</span>ел</td>
<td style="width: 55.48px; text-align: center; height: 40px;">скот</td>
<td style="width: 55.52px; text-align: center; height: 40px;">скотч.</td>
</tr>
<tr style="height: 40px;">
<td style="width: 301px; text-align: left; height: 40px;"><strong>&nbsp;Слово целиком, или окончание слова:</strong><br />&nbsp;*кот=КОТ</td>
<td style="width: 55px; text-align: center; height: 40px;"><span style="text-decoration: underline;">КОТ</span></td>
<td style="width: 55px; text-align: center; height: 40px;">котел</td>
<td style="width: 55.48px; text-align: center; height: 40px;">с<span style="text-decoration: underline;">КОТ</span></td>
<td style="width: 55.52px; text-align: center; height: 40px;">скотч.</td>
</tr>
<tr style="height: 3.84px;">
<td style="width: 301px; height: 3.84px;"><strong>&nbsp;Слово целиком, или часть&nbsp;слова:</strong><br />&nbsp;*кот*=КОТ</td>
<td style="width: 55px; text-align: center; height: 3.84px;"><span style="text-decoration: underline;"> КОТ</span></td>
<td style="width: 55px; text-align: center; height: 3.84px;"><span style="text-decoration: underline;"> КОТ</span>ел</td>
<td style="width: 55.48px; text-align: center; height: 3.84px;">с<span style="text-decoration: underline;">КОТ </span></td>
<td style="width: 55.52px; text-align: center; height: 3.84px;">с<span style="text-decoration: underline;">КОТ</span>ч.</td>
</tr>
<tr style="height: 20px;">
<td style="width: 301px; text-align: left; height: 20px;">&nbsp;<strong>Начало слова:</strong><br />&nbsp;кот&amp;=КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;"><span style="text-decoration: underline;">КОТ</span>ел</td>
<td style="width: 55.48px; text-align: center; height: 20px;">скот</td>
<td style="width: 55.52px; text-align: center; height: 20px;">скотч.</td>
</tr>
<tr style="height: 20px;">
<td style="width: 301px; text-align: left; height: 20px;">&nbsp;<strong>Окончание слова:</strong><br />&nbsp;&amp;кот=КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">котел</td>
<td style="width: 55.48px; text-align: center; height: 20px;">с<span style="text-decoration: underline;">КОТ</span></td>
<td style="width: 55.52px; text-align: center; height: 20px;">скотч.</td>
</tr>
<tr style="height: 20px;">
<td style="width: 301px; text-align: left; height: 20px;">&nbsp;<strong>Часть в середине&nbsp;слова:</strong><br />&nbsp;&amp;кот&amp;=КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">котел</td>
<td style="width: 55.48px; text-align: center; height: 20px;">скот</td>
<td style="width: 55.52px; text-align: center; height: 20px;">с<span style="text-decoration: underline;">КОТ</span>ч.</td>
</tr>
<tr style="height: 20px;">
<td style="width: 301px; text-align: left; height: 20px;">&nbsp;<strong>Начало или часть в середине слова:</strong><br />&nbsp;*кот&amp;=КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;"><span style="text-decoration: underline;">КОТ</span>ел</td>
<td style="width: 55.48px; text-align: center; height: 20px;">скот</td>
<td style="width: 55.52px; text-align: center; height: 20px;">с<span style="text-decoration: underline;">КОТ</span>ч.</td>
</tr>
<tr style="height: 20px;">
<td style="width: 301px; text-align: left; height: 20px;">&nbsp;<strong>Окончание или часть в середине слова:</strong><br />&nbsp;&amp;кот*=КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">КОТ</td>
<td style="width: 55px; text-align: center; height: 20px;">котел</td>
<td style="width: 55.48px; text-align: center; height: 20px;">с<span style="text-decoration: underline;">КОТ</span></td>
<td style="width: 55.52px; text-align: center; height: 20px;">с<span style="text-decoration: underline;">КОТ</span>ч.</td>
</tr>
<tr style="height: 20px;">
<td style="width: 301px; text-align: left; height: 20px;">&nbsp;<strong>Символ $ в начале шаблона включает режим сравнения с учетом регистра*:</strong><br />&nbsp;$Кот<span class="GramE">=К</span>о&lt;т</td>
<td style="width: 55px; text-align: center; height: 20px;"><u>Ко&lt;т</u></td>
<td style="width: 55px; text-align: center; height: 20px;">кот</td>
<td style="width: 55.48px; text-align: center; height: 20px;">кОт</td>
<td style="width: 55.52px; text-align: center; height: 20px;">КОТ</td>
</tr>
</tbody>
</table>
 
 
  
  #### Структура папок в программме
 Папка Dic состоит из трёх частей:
 1. Папка 1 - папка предварительной обработки текста
 2. Папка 2 - папка постобработки текста
 3. Папка Dic - папка со словарями
 
 В папке 1 производится предварительная обработка текста. Правила в данной папке выполняются самыми первыми. Правила следуют друг за другом "по цепочке", вносят изменения в текст и не "резервируются" (см. ниже). В данной папке производится:
 - очистка текста от лишних скобок, пробелов, расстановка дополнительных пробелов и т.п.
 - замена сокращений словами, подготовка аббривиатур к прочтению
 - замена аббривиатур, литер имени и отчества произносимым текстом (ДТП -> дэ-тэпэъ<, Е.А. Гуляев ->  Еэъ Аъ Гуляев)
 - замена слова написанных заглаными буквами словом, написанным строчными буквами (СОЛНЦЕ -> Солнце)
 - расстановка ударений в словосочениях из двух и более слов (мертворожденный -> мертворождёънный, красно-серое -> краъ<сно-сеъ<рое)
 
 В папке 2 производится корректировка отдельных ошибок произношения слов движком Digalo Nikolai 5.1. Правила в данной папке выполняются самыми последними, после того, как все правила уже отработали и внесли свои изменения в текст. 
 
 В папке Dic производится основная обработка текста правилами. Словари в ней предназначены для расстановки ударений в словах, а так же для склонения числительных. Алгоритм применения правил является "выборочным":
 - На первом этапе производится последовательный поиск индексов соответствий для каждого правила. При первом нахождении фрагмент текста (слово, часть слова, или словосочетание) «резервируется» за соответствующим правилом. При соответствии более поздних правил тому же самому фрагменту (частично или полностью), их результат не будет учитываться.
 - Таким образом, правила, расположенные раньше в порядке загрузки обладают более высоким "приоритетом" в очереди. Это позволяет организовать коллекцию словарей таким образом, что наиболее точные правила (например, регулярные выражения для омографов в контексте), расположенные "выше" всегда будут предпочтительнее менее точных ("обобщенных") правил из словарей в конце списка.
 - Так же метод "выборочной" обработки исключает возможность нежелательных замен «по цепочке», когда результат замены одного правила соответствует шаблону другого правила, идущего после него.
 
Кроме того, данный алгоритм включает оптимизацию для "простых" правил из одного слова, позволяющую существенно ускорить обработку при большом количестве правил такого вида.
В случае наличия повторных "простых" правил (с одинаковым шаблоном) в пределах всей группы, для обработки будет загружен только один экземпляр, расположенный ранее в общем порядке загрузки.

В папке Dic производится обработка текста по следующему алгоритму:
1. 01_clean_2 - удаление символов, оставшихся поле предобработки из папки 1; перевод символов из вернего регитсра в нижний.
2. 02_Числительные - перевод чисел в различных выражениях в тексте в текстовый формат, в правильном склонении.
3. 03_Исключения_перед_REX_ами - простые выражения с омографами, которые сложно описать регулярными выражениями (далее REX).
4. 04_Простые_выражения - правила замены одного простого выражения другим простым выражением с расставленными ударениями. В данном словаре ни в каком виде не должны присутствовать выражения со звёздочками.
5. 



