# Руководство по описанию блоков библиотек `О2`

<!-- TOC -->

## Введение

Данное руководство описывает принципы разработки документации и структуру описания блоков библиотеки `bem-components`.

Документация (спецификация) блоков входит в состав кода библиотеки. Версионируется с библиотекой по правилам [семантического версионирования](http://semver.org/lang/ru/).

Документация блока пишется на русском и английском языках в формате [Github Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/), в соответствии с [шаблоном](template.md), и хранится в директории блока `blockName` в файле `blockName.ru.md` и `blockName.en.md`.

**Шаблон** содержит рекомендуемую структуру документации блока.

**Целевая аудитория документа** — разработчики веб-приложений.

**Документы, рекомендуемые для предварительного ознакомления**

[Оформление документации]()

[Шаблон](template.md)

**Основные принципы разработки документации:**

* **Краткость и лаконичность**<br>
    В документации описан минимум информации, необходимой пользователю, чтобы использовать блок из библиотеки.
* **Ориентация на читателя**<br>
    Наличие краткой и подробной информации по каждой сущности блока позволяет знающему пользователю быстро освежить информацию в памяти, а новичку – вникнуть в детали каждой сущности.
* **Удобство пользования**<br>
    Представление данных как в табличном, так и текстовом формате дает возможность быстро увидеть все сущности, из которых состоит блок, и перейти к конкретным деталям каждой сущности в пределах одного документа.
* **Инлайновые примеры**<br>
    Использование каждой сущности показано на собранном рабочем примере непосредственно рядом с описанием.

## Структура документации к блоку

Документ состоит из трех основных разделов:

* [Определение функциональности блока](#block-definition)
* [Обзор блока](#block-overview)
* [Описание блока](#block-description)

<a name="block-definition"></a>
### Краткое описание

Не выделяется как отдельный раздел документа. Текст начинается сразу после названия блока.

Содержит короткое описание того, для чего используется блок. Чаще всего это одно предложение, которое начинается с фразы «Используется для ...».

При наличии нескольких версий блока, краткое описание содержит основные отличия от предыдущей версии и совместимость с другими версиями.

____________________

**Какие задачи решает:**

* Позволяет быстро ориентироваться при выдаче краткой информации по поисковому запросу для нужного блока за счет унифицированного описания.
* Облегчает выбор нужной версии блока по результатам быстрого поиска. Переход на страницу блока и поиск отличий и совместимости не требуется.

____________________

<a name="block-overview"></a>
### Обзор блока

Содержит разделы со сжатой информацией обо всех сущностях блока в табличном виде. Каждый раздел оформляется заголовком третьего уровня.

Последовательность:

* Модификаторы блока;
* Специализированные поля блока;
* Элементы блока;
* Модификаторы элементов блока;
* Специализированные поля элементов блока.

Наличие таблиц определяется данными блока. Например, если у блока нет элементов, то таблица «Элементы блока» в документе отсутствует.

Содержание таблиц может меняться в зависимости от новых требований или расширения функциональности блоков. Для версии `v2` библиотеки `bem-components` зафиксирован следующий набор данных для каждого типа таблиц:

<a name="block-mods"></a>
##### Модификаторы блока

* **Модификатор** – название модификатора. Оформляется ссылкой на подробное описание с примером.
* **Допустимые значения** – все допустимые значения данного модификатора.
* **Способы использования** – все возможные варианты установки данного модификатора (`JS`, `BEMJSON`).
* **Описание** – короткое описание модификатора и условия его применения.

Последовательность перечисления модификаторов в таблице определяется степенью их воздействия на блок: выше в таблице указаны модификаторы, изменяющие тип и поведение блока, ниже – внешний вид. При этом, модификаторы, влияющие на внешний вид блока, описываются после модификатора `theme`.

Для версии `v2` библиотеки `bem-components` зафиксирована следующая последовательность основных модификаторов: `type`, `mode`, `disabled`, `focused`, `togglable`, `pressed`, `hovered`, `theme`, `size`, `view`.

**Пример таблицы**

| Модификатор | Допустимые значения | Способы использования | Описание |
| ----------- | ------------------- | -------------------- | --------- |
| <a href="#anchor">type</a> (ссылка на соответствующий раздел с подробным описанием) | <code>'link'</code>, <code>'submit'</code> | <code>BEMJSON</code> | Тип кнопки.|

<a name="#block-fields"></a>
##### Специализированные поля блока

* **Поле** – название поля. Оформляется ссылкой на подробное описание с примером.
* **Тип** – тип данных (`string`, `number`, `boolean`, `array`, `BEMJSON`).
* **Описание** – короткое описание поля и условия его применения.

Для версии `v2` библиотеки `bem-components` зафиксирована следующая последовательность основных полей: `name`, `val`, `text`, `url`, `icon`, `title`, `id`, `tabIndex`. Поля перечисляются по степени важности для каждого конкретного блока: от большей к меньшей.

**Пример таблицы**

| Поле | Тип | Описание |
| ---- | --- | -------- |
| <a href="#anchor">name</a> (ссылка на соответствующий раздел с подробным описанием) | <code>String</code> | Уникальное имя блока. Не используется, если <a href="#anchor">модификатор type выставлен в значение link</a> (ссылка на соответствующий раздел с подробным описанием). |

##### Элементы блока

* **Элемент** – название элемента. Оформляется ссылкой на подробное описание с примером.
* **Способы использования** – все возможные варианты использования данного элемента (`JS`, `BEMJSON`).
* **Описание** – короткое описание элемента и условия его применения.

**Пример таблицы**

| Элемент | Способы использования | Описание |
| ------- | -------------------- | --------- |
| <a href="#anchor">group</a> (ссылка на соответствующий раздел с подробным описанием) | <code>BEMJSON</code> | Визуальная группировка пунктов меню. |

##### Модификаторы элементов блока

Таблица модификаторов элементов блока содержит для каждого элемента тот же набор данных, что и таблица [Модификаторы блока](#block-mads).

##### Специализированные поля элементов блока

Таблица специализированных полей элементов блока содержит для каждого элемента тот же набор данных, что и таблица [Специализированные поля блока](#block-fields).

____________________

**Какие задачи решает:**

* Позволяет быстро ориентироваться во всем многообразии модификаторов, элементов и полей блока.
* Позволяет быстро получить необходимый минимум информации по блоку.
* Облегчает поиск подробной информации по блоку, так как выполняет роль содержания документа.

____________________

<a name="block-description"></a>
### Описание блока

Содержит подробное описание блока и всех его сущностей.

Имеет такую же последовательность вложенных разделов, как и раздел [Обзор блока](#block-overview).

Каждая сущность блока (модификатор, элемент, поле) оформляется отдельным вложенным разделом с заголовком четвертого уровня и содержит набор обязательных данных.

Принципы подробного описания сущностей блока:

#### Оформление заголовка

Соответствует всем базовым [правилам оформления заголовков](#).

Заголовок обязательно содержит указание на тип сущности (модификатор, элемент, поле) и название сущности, заключенное в бэктики.

Например:

```
#### Модификатор `type`
```

Все значения модификаторов блока блока должны быть описаны. Для этого используется подзаголовок пятого уровня, который оформляется следующим образом:

```
##### Смысловое название блока с примененным модификатором (модификатор `название модификатора` в значении `значение`)
```

```
##### Поле для ввода пароля (модификатор `type` в значении `password`)
```
____________________

**Какие задачи решает:**

* Дает полную информацию о каждой сущности независимо от того, в какой части документа находится читатель.

Дублирование типов сущностей (модификатор, элемент, поле) в заголовках обусловлено наличием большого числа перекрестных ссылок в документе. Читатель всегда должен получать полную информацию о том, в каком разделе документа он находится.
____________________


#### Описание

Содержит обязательные данные для каждой сущности. Набор данных может изменяться в зависимости от требований и изменений в функциональности блока, но должен совпадать с набором данных из таблиц в разделе [Обзор блока](#Обзор блока).

**Описание должно содержать:**
* [набор обязательных данных](#mandatory-data);
* все особенности поведения блока;
* все возможные варианты применения модификатора/элемента/поля в зависимости от других установленных сущностей.

**Не включается в описание:** изменение внешнего вида блока, связанное с применением к блоку той или иной темы. Эти особенности должны быть описаны в отдельном документе к каждой теме.

<a name="mandatory-data"></a>
**Набор обязательных данных**

Для версии `v2` библиотеки `bem-components` зафиксирован следующий набор обязательных данных:

| **Модификаторы блока / элемента** | **Поля блока / элемента** |
|-----------------------------------|---------------------------|
| Допустимое(ые) значение(я): | Тип: |
| Способ(ы) использования: |  |

При наличии у блока значения по умолчанию, необходимо его указывать.

Обязательные данные указываются в начале описания сущности блока.

Например:

```
#### Модификатор `type`

Допустимые значения: `'password'`, `'search'`.

Способ использования: `BEMJSON`.
```

#### Встроенные примеры

Описание каждой сущности сопровождается примером – фрагментом `BEMJSON`, демонстрирующим применение конкретного модификатора.

Правила оформления примеров описаны в документе [Оформление документации](#).

При сборке документации для выкладки на сайт с документацией, фрагмент `BEMJSON` преобразуется в  полноценный пример, позволяющий увидеть внешний вид блока для каждого конкретного случая и продемонстрировать его поведение.

Сложные примеры, требующие дополнительной обвертки и применения JavaScript, выносятся в отдельную вкладку **Примеры**.
