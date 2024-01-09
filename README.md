# Дипломный проект на курсе «HTML-вёрстка: с нуля до первого макета»

В рамках дипломного проекта нужно сверстать макет сайта, который выглядит, как на скрине:
 
 ![](sources/NOEMI_Modern_ru.jpg)

## Требования к дипломному проекту

#### Содержание
1. [Кроссбраузерная вёрстка](#Кроссбраузерная-вёрстка).
2. [Семантическое использование тегов](#Семантическое-использование-тегов).
3. [Использование тегов для стилизации элементов](#Использование-тегов-для-стилизации-элементов).
4. [Семантические названия атрибутов](#Семантические-названия-атрибутов).
5. [Соответствие вёрстки макету](#Соответствие-верстки-макету).
6. [Добавление меньшего или большего количества контента в блоки](#Добавление-меньшего-или-большего-количества-контента-в-блоки).
7. [Высота элементов должна рассчитываться по контенту](#Высота-элементов-должна-рассчитываться-по-контенту).
8. [Вёрстка однотипных элементов](#Вёрстка-однотипных-элементов).
9. [Требования к поведению элементов в проекте](#Требования-к-поведению-элементов-в-проекте).
10. [Ошибки загрузки изображений](#Ошибки-загрузки-изображений).
11. [Вёрстка текста, написанного заглавными буквами](#Вёрстка-текста-,-,написанного-заглавными-буквами).
12. [Вёрстка декоративных линий у заголовков](#Вёрстка-декоративных-линий-у-заголовков).
13. [Вёрстка маски для изображений](#Вёрстка-маски-для-изображений).
14. [Отсутствие пустых тегов в HTML](#Отсутствие-пустых-тегов-в-HTML).
15. [Вёрстка отступов](#Вёрстка-отступов).
16. [Вёрстка иконок](#Вёрстка-иконок).
17. [Вёрстка скрытого текстового описания у полей ввода](#Вёрстка-скрытого-текстового-описания-у-полей-ввода).
18. [Запрещается использовать CSS-методологии](#Запрещается-использовать-CSS-методологии).
19. [Запрещается использовать готовые библиотеки](#Запрещается-использовать-готовые-библиотеки).
20. [Запрещается использовать CSS-препроцессоры или PostCSS](#Запрещается-использовать-CSS-препроцессоры-или-PostCSS).
21. [Запрещается использовать autoprefixer](#Запрещается-использовать-autoprefixer).
22. [Запрещается использовать `float` и `inline-block` не по прямому назначению](#запрещается-использовать-float-и-inline-block-не-по-прямому-назначению).
23. [Оформление кода](#Оформление-кода).
24. [Реализация дипломного проекта в CodePen](#Реализация-дипломного-проекта-в-Codepen).

### Кроссбраузерная вёрстка

Свёрстанный макет должен корректно отображаться на компьютерах с операционными системами Microsoft Windows и macOS.

Кроме поддержки основных типов ОС вёрстка также должна работать корректно в **последних версиях** браузеров:
- Google Chrome;
- Mozilla FireFox;
- Microsoft Edge;
- Opera;
- Safari.

Если у вас нет нужного устройства для тестирования, постарайтесь его найти. Тестирование на реальных устройствах — обязательный навык современного специалиста.

### Семантическое использование тегов

При вёрстке проекта преимущество отдаётся тегам, имеющим смысл. Например, будет ошибкой, если сверстать раздел «Новости» так:

```html
<div class="news">
  <h2>Новости</h2>
</div>
```

В этом примере нужно использовать тег `section`:

```html
<section class="news">
  <h2>Новости</h2>
</section>
```

### Использование тегов для стилизации элементов

Запрещается использовать теги в целях стилизации элементов. Например, если сверстать жирный текст тегом `b`, то это будет ошибкой.

```html
<b>Текст</b>
```

### Семантические названия атрибутов

Кроме использования семантических тегов также нужно давать семантические названия значениям атрибутов. Запрещается использовать транслит.

Пример:

```html
 <header class="shapka"></header>
```

Этот пример — грубая ошибка. Название класса `shapka` нужно заменить на `header`. 

Пример корректного названия:

```html
 <header class="header"></header>
```

При именовании классов можно использовать принятый [список классов](https://github.com/yoksel/common-words).  

### Соответствие вёрстки макету

Итоговый проект должен быть копией макетов от дизайнера. При реализации допускаются отличия:
- толщина шрифта в браузерах и фотошопе;
- межсимвольное расстояние;
- различия в отступах — до 3px.

### Описание отображения страницы 

Дизайнер подготовил макет шириной 1660px, но, несмотря на это, вам нужно предусмотреть отображение макета на экранах с шириной  больше, чем 1660px. Для этого дизайнер подготовил требования:
- изображение в шапке должно занимать всю ширину экрана;
- контент в шапке должен быть выровнен по центру;
- блок, содержащий контент в шапке, должен иметь отступы по бокам;
- блок, содержащий основную часть страницы, должен иметь отступы по бокам;
- подвал страницы должен иметь отступы по бокам.

### Добавление меньшего или большего количества контента в блоки

Вам обязательно нужно протестировать блоки с информацией, добавив в них больше или меньше контента, чем дано в макетах. Блоки не должны сломать соседние блоки, текст должен быть полностью читаемым. 

Вам нужно предусмотреть случаи:
- добавление двух пунктов в меню;
- удаление  двух, трёх, четырёх пунктов из меню;
- добавление двух–трёх слов в заголовке «Блог о творчестве, спорте и образе жизни»;
- добавление двух блоков со статьёй;
- удаление всех блоков со статьями, кроме первого; 
- добавление трёх абзацев текста в блоке со статьёй;
- теги статьи могут располагаться на  двух строках;
- имя автора статьи может быть длиннее и короче, чем в макете;
- дата статьи может быть длиннее и короче, чем в макете;
- добавление двух статей в разделе «Новые посты»;
- удаление всех статей в разделе «Новые посты», кроме первой;
- удаление любого блока из следующих: блок «Новые посты»,  форма поиска, блок «Рассылка», блока «Теги», блок «Темы»;
- отображение восьми иконок соцсетей;
- отображение трёх иконок соцсетей.

### Высота элементов должна рассчитываться по контенту

При вёрстке элементов не нужно фиксировать их высоту — высота должна зависеть от контента внутри элемента. Это нужно для осуществления пункта [«Добавление меньшего или большего количества контента в блоки»](#Добавление-меньшего-или-большего-количества-контента-в-блоки). 

Разрешается фиксировать высоту для декоративных элементов: черта под заголовками, иконки, кнопки в форме поиска, поля ввода в формах.

Также при вёрстке элементов нужно следить, чтобы у элементов свойство `height` не равнялось 0, а также зависело от контента.

### Вёрстка однотипных элементов

При работе с макетом вы можете столкнуться с ситуацией, когда у однотипных элементов отличается ширина или другое свойство на несколько пикселей. Например, ширина элементов статей в разделе «Новые посты». Визуально они отличаются. 

Это сделано, чтобы посмотреть, как будет отображаться разный текст. В вашей вёрстке ширина у этих элементов должна быть одинаковой. Можете выбрать самостоятельно один из размеров макета и задать его для всех однотипных элементов. Не нужно подгонять каждый элемент под размеры макета.

### Требования к поведению элементов в проекте

Вы должны предусмотреть сценарии поведения элементов:
- все пункты в меню должны быть ссылками;
- все заголовки статей должны быть ссылками;
- все формы на странице должны отправлять данные;
- все формы на странице должны проверять корректность введённых данных;
- все теги на странице должны быть ссылками;
- в блоке «Темы» каждое название категории должно быть ссылкой;
- в блоке «Темы» количество статей в категории должно быть текстом;
- иконки соцсетей должны быть ссылками;
- копирайт на странице должен быть ссылкой.

Для всех ссылок на странице используйте атрибут `href` со значением `#0`.

### Ошибки загрузки изображений

При вёрстке изображений нужно предусмотреть ситуацию, когда по какой-либо причине они не загрузятся.

1. В случае контентных изображений вёрстка не должна сломаться, а вместо изображения должен отображаться альтернативный текст, из которого станет понятно, что было изображено на картинке.
2. Для декоративных изображений вам нужно подобрать подложки для текста, чтобы текст был читаемым в любой ситуации.

### Вёрстка текста, написанного заглавными  буквами

Заглавное отображение текста должно быть реализовано с использованием CSS. Запрещается писать текст только заглавными в HTML. Пример ошибки:

```html
    <h3>ЭТО ЗАГОЛОВОК</h3>
```

### Вёрстка декоративных линий у заголовков

Декоративное подчеркивание у заголовков «Новые посты», «Рассылка», «Теги» и др. нужно реализовать через псевдоэлементы.  

### Вёрстка маски для изображений

Маску для изображений нужно реализовать через псевдоэлементы.

### Отсутствие пустых тегов в HTML

В HTML у вас не должно быть тегов без контента.

### Вёрстка отступов

Нужно внимательно реализовывать отступы. Внешние отступы задаются между соседними элементами, а внутренние — между родителем и дочерним элементом. Несоблюдение этого правила будет ошибкой. 

### Вёрстка иконок

Все иконки в проекте должны иметь скрытое текстовое описание. Для скрытия текста используйте код:

```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  border: 0;
  clip: rect(0 0 0 0);
  overflow: hidden;
} 
```


### Вёрстка скрытого текстового описания у полей ввода

Визуальное текстовое описание полей ввода не предусмотрено дизайнером. Поэтому нужно самостоятельно его придумать и скрыть, используя класс `visually-hidden` из предыдущего пункта.

Текстовое описание должно понятно объяснять, какие данные нужно вводить в поля. Оно должно быть задано и для кнопки поиска, так как на кнопке нет текста.

### Запрещается использовать CSS-методологии 

На курсе мы не рассматриваем CSS-методологии: БЭМ, OOCSS, SMACSS и другие, поэтому в дипломе запрещается их использовать. 

### Запрещается использовать готовые библиотеки

В рамках дипломного проекта запрещается использовать готовые библиотеки, например, normalize.css, reset.css, bootstrap и другие. Весь код вы должны написать самостоятельно.

### Запрещается использовать CSS-препроцессоры или PostCSS

На курсе  мы не рассматриваем способы организации кода с использованием CSS-препроцессоров и PostCSS, поэтому в дипломе запрещается их использовать.

### Запрещается использовать autoprefixer

Для реализации кроссбраузерной вёрстки дипломного проекта вам не нужен autoprefixer, поэтому его использование запрещено.

### Запрещается использовать `float` и `inline-block` не по прямому назначению

`float` был создан и должен использоваться для позиционирования картинок внутри текста. `inline-block` также не подойдёт для выстраивания блоков в строку. Для таких задач существует технология flexbox. Именно ей и нужно отдавать предпочтение при вёрстке диплома.

### Оформление кода

Дипломный проект обязательно должен соответствовать принятому стилю кода для [HTML](https://github.com/netology-code/codestyle/tree/master/html) и [CSS](https://github.com/netology-code/codestyle/tree/master/css). Если будут ошибки в оформлении, проект отправится на доработку.

### Порядок следования CSS-правил 

При реализации проекта порядок CSS-правил должен совпадать с порядком следования элементов в HTML. Например, есть HTML:

```html
    <header class="header">
      <h1 class="header-title">Заголовок</h1>
    </header>
    <main class="main">
      <section class="section">
        <h2 class="section-title">Новости</h2>
      </section>
    </main>
```

Для стилизации структуры нужно использовать порядок CSS-правил:

```css
    .header { 
      padding: 10px;
    }
    
    .header-title {
      font-size: 20px;
    }
    
    .main {
      margin-left: auto;
      margin-right: auto;
    }
    
    .section {
      background-color: #eeeeee;
    }
    
    .section-title {
      font-size: 18px;
    }
```

### Реализация дипломного проекта в CodePen

Дипломный проект должен быть реализован на сайте CodePen. Вам не нужно создавать основной каркас страницы. Во вкладке HTML создайте сразу разметку страницы без элемента `body`. Для подключения декоративных элементов, изображений и шрифтов проекта используйте ссылки из файла [«Ресурсы проекта»](sources/README.md).

### Мой проект вы можете посмотреть:
1. [В CodePen](https://codepen.io/ilyapatis24/pen/ZEVVpzR?editors=1100)
2. [На GitHub Pages](https://ilyapatis24.github.io/Blog_about_creativity/)