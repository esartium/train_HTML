# Курс по html: конспект

HTML - язык гипертекстовой разметки (не программирования)
Позволяет описать, какие объекты должны быть на странице, и расставить их на странице.

Для написания html-кода подходит любой текстовый редактор.

## Основы

Основной файл должен называться "index.html"
Весь html состоит из <тегов>.

```
<html> <!-- в начале прописываем основной тег 
    (открывающий; все остальные теги будут
    между этим тегом и закрывающим) -->

<head> 
    это шапка сайта (описание характеристик  сайта, например, название/описание страницы, 
    ключевые слова страницы, указание, кто автор
    страницы и т.д.; пользователь не видит этого,
    шапку видят только только роботы, например, 
    поисковики)
</head>

    <body> 
        пользователь видит всё, 
        что прописано в этом теге
    </body>

</html> <!-- в конце ставим закрывающий основной тег -->
```

HTML-файл по умолчанию открывается в браузере (нужно просто его сохранить и дважды кликнуть на него)

Внутри тега head пишется тег title:

```
<head>
<title>
    Этот тег отвечает за название страницы 
    (которое указано на вкладке браузера);
    среди всего, что есть внутри тега head, 
    это единственное, что видит пользователь
</title>
</head>
```

Чтобы вместо текста не выводилась белиберда, внутри тега head нужно установить кодировку:

```
<html>
    <head>
        <meta charset="utf-8">
        <title>
            вкладка
        </title>
    </head>
    <body>
        букавы
    </body>
</html>
```

Кодировка устанавливается внутри head, так как, по сути, относится к настройкам страницы. Данный тег одинарный, к нему не нужен закрывающий.

Теги, начинающиеся с "meta" - это теги, отвечающие за настройки метаданных.

"utf-8" - одна из возможных кодировок; их много: какие-то поддерживают только латиницу, какие-то только кириллицу, и т.д.; utf-8 поддерживает и то, и то.

Также в html-документах всегда прописывается версия html, используемая внутри данного файла, например:

```
<!DOCTYPE html>
```

Мы указали, что внутри этого документа используется html 5 версии. Это прописывается в самом начале файла, до основного тега ` <html> `.

### Комментарии 

В html комментарии (кусочек текста, не видный пользователю; то есть это привычные комментарии в коде, как и в остальных языках) пишутся следующим образом:

```
<!-- бебебе -->
```

Такие комментарии могут быть на несколько строк.

## Метаданные

Метаданные - это настройки страницы.

Некоторые теги метаданных:

Указание кодировки:
```
<meta charset="utf-8">
```

Указание автора страницы:
```
<meta name="author" content="соня">
```

Указание описания страницы:
```
<meta name="description" content="какая-то страница">
```

Указание ключевых слов для данной страницы:
```
<meta name="keywords" content="страница,слова,html,буквы">
```

Атрибуты - расширения, которые прописываются внутри тегов. При помощи атрибутов расширяется функционал какого-либо тега. Здесь, например, атрибуты: name, charset, content и т.д.

Мета-теги не являются обязательными с точки зрения клиента и нужны в основном для поисковиков, чтобы они могли выдавать сайт в поиске.

## Теги для работы с текстом

### Заголовки на странице

```
<h1>
Заголовок первого уровня
</h1>

    <h2>
    Заголовок второго уровня
    </h2>

        <h3>
        Заголовок третьего уровня
        </h3>

            и т.д. (ВСЕГО 6 УРОВНЕЙ ЗАГОЛОВКОВ, с каждым уровнем заголовок меньше предыдущего по размеру; теги называются аналогично, в соответствии с уровнем)
```

### Абзацы

```
<p>
Абзац
</p>

<p>
А это уже другой абзац
</p>
```

Текст, написанный в этом теге, будет обычным (не жирным и т.д.)

HTML не волнуют обычные переносы текста; текст переносится только тегами.

### Стилизация текста

Жирный:
```
<b> 
b значит "ball", типа жирный гыггыгы
</b>
```

Ещё один жирный: 
```
<strong>
выведет то же самое, что и тег <b>, просто ещё один вариант
</strong>
```

Курсив:
```
<em>
bebebe
</em>
```
```
<i>
ещё один точно такой же курсив
</i>
```

Перечёркнутый текст:
```
<strike>
бебебе
</strike>
```

Индекс:
```
H<sub>2</sub>O
```

Степень:
```
a<sup>2</sup>
```

Перенос строки:
```
<br>Одиночный тег, не нужно закрывать (работает именно как перенос строки, а не как создание нового абзаца, так как не создаёт отступов от других строк).
```

Горизонтальная линия на всю ширину страницы (одиночный тег):
```
<hr>
```

Аббревиатуры:
```
<abbr>HTML</abbr>
```

Сделать, чтобы текст появлялся при наведении на слово (расшифровка аббревиатуры):
```
<abbr title="Hyper Text Mark чето там блаблабла">HTML</abbr>
```
Атрибут расшифровки можно добавлять не только к аббревиатурам. Например:
```
<h4 title="бубубу">bububu</h4>
```

Адрес (будет написан курсивом):
```
<address>
Russia, Воронеж
</address>
```

Размер текста:
```
<big>
Текст чуть больше, чем остальной
</big>
```
```
<small>
Текст чуть меньше, чем остальной
</small>
```

Кусок кода (будет выведен с сохранением всех пробелов, отступов и т.д., а также будет немного другой шрифт):
```
<pre>
for (int i = 0; i < n; i++) {
    cout << "bebebe" << "\n";
}
</pre>
```
или
```
<code>
for (int i = 0; i < n; i++) {
    cout << "отступы не сохранятся, немного изменится шрифт" << "\n";
}
</code>
```

##### замечание

Теги могут содержаться и внутри других тегов, например:

```
<p>
хаха,
<b>
жирный
</b>
</p>
```

Другие типы тегов также могут быть вложены в другие теги (важно соблюдать правильную вложенность).

## Списки

#### Нумерованные

```
<ol>
<li>первый элемент</li>
<li>второй элемент</li>
<li>третий элемент</li>
</ol>
```
(Здесь ol - ordered list, li - list item)

Атрибуты для списков:

Указать, с какого числа начинается нумерация (по умолчанию с единицы):
```
<ol start="100">
<li>первый элемент</li>
<li>второй элемент</li>
<li>третий элемент</li>
</ol>
```

Указать, каким образом будут отображаться номера элементов списка, например, чтобы была нумерация буквами a,b,c,...:
```
<ol type="a">
<li>первый элемент</li>
<li>второй элемент</li>
<li>третий элемент</li>
</ol>
```
Типы нумерации для данного атрибута можно посмотреть при вводе команды в текстовом редакторе.

#### Ненумерованные:

```
<ul>
<li>элемент</li>
<li>элемент</li>
<li>элемент</li>
</ul>
```
(Здесь ul - unordered list)

По умолчанию элементы отмечаются закрашенными кружочками. Чтобы изменить это, используется атрибут type; например, нумерация незакрашенными кружочками:
```
<ul type="circle">
<li>элемент</li>
<li>элемент</li>
<li>элемент</li>
</ul>
```
И другие варианты.

## Атрибуты

Атрибуты - расширения, которые прописываются внутри тегов; они описывают дополнительный функционал тега.

С помощью атрибута title него можно задать подсказку, которая будет показываться при наведении на объект, например:
```
<p title="какая-то подсказка">
какой-то объект
</p>
```

Атрибут title можно применять ко всем тегам. 

Исключения: `<head>` и `<html>`. К ним нельзя применять title.

К `<html>` можно добавить, например, атрибут, показывающий, какой язык используется внутри документа:
```
<html lang="ru">
...
</html>
```
Это не обязательный атрибут, от него ничего не поменяется.

Если применить title к тегу body, подсказка будет появляться при наведении на всю страницу.

К одному тегу можно прописывать больше одного атрибута (10, 20, миллиард атрибутов).

## Ссылки

######
Специальный тег для создания ссылок:
```
<a href="сама ссылка">
Текст, описывающий ссылку
</a>
```
Данный тег работает только с атрибутом href (для этого тега это обязательный атрибут)

Можно добавить и другие атрибуты, которые не являются обязательными, например, подсказку:
```
<a href="ссылка" title="подсказка">
текст, описывающий ссылку 
</a>
```

######
Также можно указать, каким образом пользователь перейдёт по ссылке:
```
<a href="ссылка" target="вариант из списка текстового редактора" title="подсказка">
текст, описывающий ссылку 
</a>
```
Текстовый редактор предлагает варианты того, как пользователь может перейти по ссылке: в той же  вкладке/в новой вкладке и т.д. (по умолчанию вкладка открывается на той же странице)

###### Перейти на другой свой html-файл
```
<a href="название_файла_из_той_же_папки.html">
текст, описывающий ссылку
</a>
```
Таким образом мы прописываем уже не ссылку, а относительный путь к файлу; мы можем так сделать для файлов, которые находятся в той же папке, что и текущий файл (из которого переходим).

###### Ссылка-якорь 
(позволяет перейти к определённому месту на этой же странице):

```
<a href="#название_якоря">
Перейти к чему-то
</a>
```

```
<a name="название_якоря"></a>
```

Якорь может быть каким угодно.

Элемент, к которому мы перемещаемся, тоже может быть любым, в том числе не только объектом на странице, но и, например, какой-то точкой на странице (то есть мы можем переместиться вверх/вниз и т.д.)

###### Ссылка на почтовый клиент:

```
<a href="mailto:почтовый_адрес">
написать на почту
</a>
```

## Изображения

Тег для работы с изображениями (одинарный тег):
```
<img src="полный путь к картинке" width="ширина" height="длина">
```

Отображаемая картинка может быть как из интернета (находим изображение в интернете и нажимаем "копировать URL"), так и из папки проекта.

Данный тег работает только при наличии атрибута src. 

Также можно указать другие необязательные6 но важные атрибуты:

Здесь:

+ width - ширина изображения; 

    Ширина указывается либо в процентах от страницы:

```
width="32%"
```

    либо в пикселях:

```
width="500px"
```

Если выставить ширину на всю страницу, небольшие отступы всё равно останутся (их можно убрать с помощью CSS-стилей).

+ height - высота изоюражения;
    Высота автоматически подстраивается под ширину, если она не указана. То же самое произойдёт, если указать:
    ```
    height="auto"
    ```
    
    Указывается, аналогично ширине, в процентах или пикселях.

Также можно прописать текст, который отобразится, если вдруг не отобразится картинка. Это делается с помощью атрибута alt:
 
```
<img src="полный путь к картинке" width="ширина" height="длина" alt="текст">
```

Картинки лучше хранить в отдельной папке, которая хранится в папке проекта.

## HTML-таблицы

###### Основная структура
Основные теги для работы с HTML-таблицами:
```
<table>
    <thead>
    ...
    </thead>
        <tbody> 
        ...  
        </tbody>
            <tfoot>
            ...
            </tfoot>
</table>
```
Здесь:

thead - шапка, tfoot - футер, tbody - основная часть.

Тег для описания какого-либо ряда:
```
<tr>
Его можно использовать в любом из тегов, приведённых выше.
</tr>
```

Внутри ряда можно создать какое-то количество столбцов.

Создать столбцы в каком-то ряду в теге thead:
```
<tr>
<th>заголовок определённого столбца</th>
<th>заголовок ещё одного столбца</th>
</tr>
```
В других тегах:
```
<tr>
<td>заголовок определённого столбца</td>
<td>заголовок ещё одного столбца</td>
</tr>
```

Отличие th от td в том, что th выделяется жирным шрифтом, как заголовок столбца, и располгается посередине столбца; а td, как содержимое столбца, не выделяется, просто помещается на свое место.

Таким образом, в таблице есть три "отделения", и в каждом из них может быть какое-то количество рядом и столбцов. 

Внутри тега tr пишутся теги td или th, то есть внутри каждого ряда(строки) прописывается, какие там столбцы.

###### Базовые атрибуты HTML-таблиц

Разделить содержимое таблицы можно с помощью атрибутов:
```
<table border="1">
</table>
```
Здесь указано, что таблица имеет обводку с толщиной линии 1 пискель.

Указать ширину таблицы:
```
<table width="500px">
</table>
```

Выравнивание текста (можно указать как для всей таблицы, так и для отдельного её элемента):
```
<table align="center">
<!-- Выровняли по центру всю таблицу (не текст в ячейках, а прям вся таблица посередине страницы будет) -->
</table>
```
или
```
<tbody align="center">
<!-- Выровняли по центру ячейки текст этой части таблицы -->
</table>
```

Обычно таблицы оформляются не через атрибуты, а через CSS-стили.

## Теги для подключения CSS- и JS-файлов

### CSS-файлы

Подключаются через тег link в шапке в теге head.
Тег link одинарный; работает только с атрибутами.

```
<head>
    <link rel="stylesheet" href="путь к файлу">
</head>
```

Здесь:

+ `rel="stylesheet"` означает, что мы таким образом подключаем таблицу стилей
+ в атрибуте href указывается полный путь к файлу (либо ссылка на файл из интернета, либо полный путь к файлу из папки; обычно такие файлы хранятся в папке проекта в папке с названием CSS)

Пример:
```
<head>
    <link rel="stylesheet" href="CSS/main.css">
</head>
```

### Файлы Java Script

Тег script для подключения js-файлов можно прописать как в head, так и в body (сами решаем, но принято в body (в самом его конце, перед закрытием), потому что js может тормозить загрузку html-страницы (пусть тогда будет сначала прочитан весь остальной код, а потом уже js)).

+ Вариант 1:
```
<script>
<!-- js-код можно писать прямо здесь -->
</script>
```
+ Вариант 2: подключение js-файла:
```
<script src="полный или относительный путь к файлу">
</script>
```

## Теги div и span

Не обладают никакими свойствами (просто пишут обычный текст с новой строки), пока к ним не добавлены CSS-стили.

###### div

div создаёт определённый блок; через CSS к этому блоку можно добавить любые стили (ширину, обводку и т.д.)

```
<div> просто текст с новой строки </div>
```

###### span

span без CSS выводит просто текст, не с новой строки;

При использовании CSS он позволяет добавить стили к определённой части блока; применяется внутри div:

```
<div> текст с новой <span>строки</span></div>
```

## HTML-формы и поля для ввода

Теги, нужные для работы с формами, пишутся в теге form (двойной тег):
```
<form>
<!-- тут все теги, нужные для создания формы -->
</form>
```

###### Обязательные атрибуты тега form:

```
<form action="..." method="post">
...
</form>
```

Здесь:

+ В action указывается страница, на которой будет происходить обработка формы (то есть, куда отправятся данные после того, как пользователь нажмёт "отправить");
если не указать атрибут action, данные будут обрабатываться на той же странице, где находится сама форма

+ method - метод передачи данных:
    + post (обычно используется именно он)
    + get 

###### Теги для создания формы

Общий вид:
```
<form>
    <label for="айди">Подпись для какого-либо поля</label>
    <input type="text" placeholder="подсказка" value="какой-то текст" maxlength="10" name="user_name" id="айди" hidden disabled readonly>
</form>
```

Здесь:

+ label содержит подпись для описания поля
Атрибут для тега label:

for - при нажатии на текст выделяется поле для ввода

+ input - одинарный тег для создания самого поля; имеет атрибуты, вот некоторые из них:
    + type - тип поля (например, текстовое)
    + placeholder - подсказка (например: "введите то-то"); исчезает, когда пользователь начнёт ввод
    + value - какой-то текст, который уже сразу введён в поле (пользователь может что-то дописать к нему, а также может его стереть)
    + maxlength - максимальное число допустимых символов для ввода (ввести больше не получится)
    + если добавить атрибут hidden, то поле для ввода не будет отображаться (буде скрыто)
    + если добавить атрибут disabled, то поле будет отображаться, но в него ничего нельзя будет ввести
    + если добавить атрибут readonly, то пользователю можно будет только считывать значения из текстового поля и нельзя будет туда что-то записывать
    + атрибут name="username" нужен для работы с серверным языком, чтобы по значению определённого атрибута (здесь значение "user_name"), например, name, найти и использовать определённое поле
    + id - уникальный идентификатор какого-либо объекта; такой можно установить для любого объекта(тега); понадобится для идентификации объекта для работы, например, с CSS; id не должен повторяться у объектов одной страницы

###### Форматы полей

Помимо текста существует возможность ввести пароль, выбрать цвет, дату, время и т.д.

Все эти поля создаются так же, как и текстовые; разница лишь в установленном для атрибута type значении.

Для одного label может быть несколько input, например, чтобы ввести имя пользователя и пароль, можно к одному label добавить два input различных типов: текст и пароль.

Для данных, для которых существуют свои типы полей (email, url и т.п.), лучше использовать эти типы, а не текст.

Поле типа color может не работать в некоторых браузерах (Internet Explorer, Edge, Firefox и т.п.) => если есть возможность не использовать это поле, то лучше его не использовать.

Аналогично с полем для ввода даты.

Отличие кнопок:

+ Тип button - обычная кнопка; при нажатии не обновляется страница, то есть НЕ происходит отправка данных на сервер.
+ Тип submit - кнопка, при нажатии на которую обновляеся страница и происходит отправка данных на сервер.

Тип кнопки reset - очистка всех введённых пользователем в данной форме данных.

###### Поле для ввода большого текста

```
<form>
    <textarea></textarea>
</form>
```

Получится поле размером больше стандартного, его можно будет самостоятельно растягивать по ширине и высоте, и в него можно вводить большие объёмы текста.

Для этого тега работают все те же атрибуты, что и для остальных тегов для работы с формамм. Исключение: не работает value; здесь, чтобы в поле был сразу введён какой-то текст, нужно написать его не в value, а между открывающим и закрывающим тегами textarea.

Атрибут name можно добавлять только к input и textarea.

Атрибут required делает так, что форму нельзя будет отправить на сервер, пока пользователь не ввёл туда что-то.

###### Создание кнопки

Создание кнопки без input:

Тег button:

```
<form>
    <button type="что делает кнопка">
        Здесь пишется описание действия, которое происходит при нажатии
    </button>
</form>
```

Атрибут type определяет, что будет делать кнопка (варианты: button, submit, reset).

## Селекторы выбора

Селекторы выбора создают выпадающий список с вариантами, из которых может выбирать пользователь.

Пишется:
```
<form>
    <select>
        <option>вариант 1</option>
        <option>вариант 2</option>
        <option>вариант 3</option>
        <option>вариант 4</option>
    </select>
</form>
```
Если добавить к какому-то варианту атрибут selected, то пока пользователь не выберет сам, по умолчанию будет выбран этот вариант.

Если добавить к какому-то варианту атрибут disabled, этот вариант нельзя будет выбрать.

###### Множественный выбор

Просто добавляем атрибут multiple, и тогда можно будет выбрать как один, так и несколько вариантов.

Атрибут size отвечает за то, какое количество вариантов будет сразу показано пользователю. В такой ситуации сразу нескольким вариантам можно поставить атрибут selected.

## Специальные HTML5 теги

Это теги, добавленные именно в пятую версию html (сейчас уже поддерживаются всеми основными браузерами, но некоторыми не поддерживаются).

### Теги для описания секций на странице

Например, два варианта описания шапки сайта (не той, где мета, а той, которую видит пользователь):

Вариант 1 (старый, привычный):
```
<body>
    <div id="header"></div>
</body>
```

Вариант 2(через новые HTML5-теги):
```
<header></header>
```
(Ниаких стилей тут не добавится, без CSS работает аналогично div - создаёт блок)

Основная часть сайта:
```
<main></main>
```
(Ниаких стилей тут не добавится, без CSS работает аналогично div и header - создаёт блок)

Боковая часть сайта:
```
<aside></aside>
```
(Ниаких стилей тут не добавится, без CSS работает аналогично div и header - создаёт блок)

Футер:
```
<footer></footer>
```
(Ниаких стилей тут не добавится, без CSS работает аналогично div и header - создаёт блок)

###### Теги, создающие полнофункциональный блок:

Прогресс-бар:
```
<progress>здесь может быть текст, но он обычно не отображается; отобразится, если прогресс бар не загрузится</progress>
```

Если к тегу progress не добавить атрибуты, то просто прикольная штука будет делать вжжж туда-сюда. Если добавить: см. файлик

###### Скрытый текст

Это скрытый текст, который будет показан только при нажатии на выпадающий список

```
<details>
    <summary>Текст, который показан</summary>
    Текст, который скрыт.
</details>
```

## Как за два действия написать основной html-синтаксис:

+ ввести !  

+ нажать tab

## Как сделать ссылку, при нажатии на которую ничего не будет происходить:

```
<a href="#">ссылка в никуда</a>
```