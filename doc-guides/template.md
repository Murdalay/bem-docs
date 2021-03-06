# Название блока

Блок предоставляет

        функцию, реализующую ...

        объект, содержащий набор методов для ...
        
        объект, содержащий набор свойств для ...
        
        объект, содержащий набор свойств и методов для ...
        
        объект события, дополненный набором методов (свойств) для ...
        
        компонент интерфейса для ...
        
        шаблон, создающий набор HTML-элементов ...
        
        СSS-класс, реализующий ...
        
        набор JS-классов, реализующий ...

<Краткое описание блока.>

## Обзор

<Для функций раздел "обзор" отсутствует, кроме обзора элементов.>

### События объекта

| Имя | Описание |
| -------- | -------- |
| <a href="#events-name">Имя события</a> (<i>якорь на соответствующий заголовок</i>) | Краткое описание. |

### Свойства и методы объекта (класса)

| Имя | Тип или возвращаемое значение | Описание |
| -------- | --- | -------- |
| <a href="#fields-name">Название свойства</a> (<i>якорь на соответствующий заголовок</i>) | <code>Тип данных</code> | Краткое описание. |
| <a href="#fields-name">methodName</a>(<br><code>{String} arg1</code>, <br><code>{Array} arg2</code>, <br><code>[{Boolean} argN]</code>) (<i>опциональные аргументы указываются в квадратных скобках</i>)| <code>Возвращаемое значение</code> | Краткое описание. |

### Модификаторы блока

| Модификатор | Допустимые значения | Способы использования | Описание |
| ----------- | ------------------- | --------------------- | -------- |
| <a href="#modifiers-name">Название модификатора</a> (<i>якорь на соответствующий заголовок</i>) | <code>'значение 1'</code>, <code>'значение 2'</code> | <code>BEMJSON</code>, <code>JS</code> (<i>Выберите нужное значение</i>) | Краткое описание. |

### Специализированные поля блока

| Поле | Тип | Описание |
| ---- | --- | -------- |
| <a href="#declfields-field">Название поля</a> (<i>якорь на соответствующий заголовок</i>) | <code>Тип данных</code> | Краткое описание. |

### Элементы блока

| Элемент | Способы использования | Описание |
| --------| --------------------- | -------- |
| <a href="#elems-name">Название элемента</a> (<i>якорь на соответствующий заголовок</i>) | <code>BEMJSON</code> | Краткое описание. |

#### Свойства и методы объекта

| Имя | Тип или возвращаемое значение | Описание |
| -------- | --- | -------- |
| <a href="#fields-name">Название свойства</a> (<i>якорь на соответствующий заголовок</i>) | <code>Тип данных</code> | Краткое описание. |
| <a href="#fields-name">methodName</a>(<br><code>{String} arg1</code>, <br><code>{Array} arg2</code>, <br><code>[{Boolean} argN]</code>) (<i>опциональные аргументы указываются в квадратных скобках</i>)| <code>Возвращаемое значение</code> | Краткое описание. |

### Специализированные поля элементов блока

| Элемент | Поле | Тип | Описание |
| ------- | ---- | --- | -------- |
| Название элемента, к которому относится описываемое поле | <a href="#elems-name-declfields-name">Название поля</a> (<i>якорь на соответствующий заголовок</i>) | <code>Тип данных</code> | Краткое описание. |

### Публичные технологии блока

Блок реализован в технологиях:

* `vanilla.js`
* `js`
* `browser.js`
* `node.js`
* `bh.js`
* `bemhtml`
* `json`
* `css`
* `svg`

*Лишнее удалить. Технологии, отсутствующие в списке, не являются публичными и не указываются*

## Подробности

<Подробное описание блока.>

<a name="events"></a>
### События объекта

<a name="fields-eventname"></a>
#### Событие `eventname`

Генерируется по ..

<Описание>

<a name="fields"></a>
### Свойства и методы объекта

<a name="fields-name"></a>
#### Поле `название свойства`

Тип: `{String}`, `{Number}`, `{Array}`, `{Boolean}`, `{Object}`, `{Function}`, `{*}`. *Выберите ожидаемый тип данных. Типы разделяется  `|`.*

<Описание>

<a name="fields-name"></a>
#### Метод `название метода`

<Описание метода.>

Принимаемые аргументы: 

* `arg1` `{String}`, `{Number}`, `{Array}`, `{Boolean}`, `{Object}`, `{Function}`, `{*}` – *Выберите ожидаемый тип данных. Для полиморфных методов типы разделяются  `|`. * <Краткое описание аргумента.> Обязательный аргумент. *Удалить, если нет. Имя и тип данных для необязательных аргументов указываются в квадратных скобках.*
Не принимает аргументов.

Возвращаемое значение: *Удалить, если нет значения или this*

Не имеет возвращаемого значения. 
Возвращает объект `this`. 
`{String}`, `{Number}`, `{Array}`, `{Boolean}`, `{Object}`, `{Function}`, `{*}`. В случае если .. –
*Выберите нужное значение.*

<Пример>

<a name="modifiers"></a>
### Модификаторы блока

<a name="modifiers-name"></a>
#### Модификатор `название модификатора`

Допустимые значения: `'значение 1'`, `'значение 2'`. *Обратите внимание, строчные значения заключаются в одинарные вертикальные кавычки и бэктики.*

Способ использования: `BEMJSON`, `JS`. *Выберите нужное значение.*

<Описание>

<a name="modifiers-name-1"></a>
##### Смысловое название блока с примененным модификатором (модификатор `название модификатора` в значении `значение 1`)

<Описание>

<Пример>

<a name="modifiers-name-2"></a>
##### Смысловое название блока с примененным модификатором (модификатор `название модификатора` в значении `значение 2`)

<Описание>

<Пример>

<a name="modifiers-name"></a>
#### Модификатор `название модификатора`

Допустимое значение: `булево значение`. *Обратите внимание, булевы значения заключаются только в бэктики.*

Способ использования: `BEMJSON`, `JS`. *Выберите нужное значение.*

<Описание>

<Пример>

<a name="declfields"></a>
### Специализированные поля блока

<a name="declfields-field"></a>
#### Поле `название поля`

Тип: `String`, `Number`, `Array`, `Boolean`. *Выберите нужный тип данных.*

<Описание>

<Пример>

<a name="elems"></a>
### Элементы блока

<a name="elems-name"></a>
#### Элемент `название элемента`

Элемент предоставляет
        функцию, реализующую ...
        объект, содержащий набор методов для ...
        объект, содержащий набор свойств для ...
        объект, содержащий набор свойств и методов для ...
        объект события, дополненный набором методов (свойств) для ...
        шаблон для ...
        набор специализированных полей для ...
        СSS-класс, реализующий ...
        JS-класс, реализующий ...

Элемент дополняет
        объект события набором методов (свойств) для ...
        базовый блок набором методов (свойств) для ...

<Описание>

<Пример>

<a name="elems-name-fields"></a>
### Свойства и методы объекта

<a name="elems-name-fields-name"></a>
#### Поле `название свойства`

Тип: `{String}`, `{Number}`, `{Array}`, `{Boolean}`, `{Object}`, `{Function}`, `{*}`. *Выберите ожидаемый тип данных. Типы разделяется  `|`.*

<Описание>

<a name="elems-name-fields-method"></a>
#### Метод `название метода`

<Описание метода.>

Принимаемые аргументы: 

* `arg1` `{String}`, `{Number}`, `{Array}`, `{Boolean}`, `{Object}`, `{Function}`, `{*}` – *Выберите ожидаемый тип данных. Для полиморфных методов типы разделяются  `|`. * <Краткое описание аргумента.> Обязательный аргумент. *Удалить, если нет. Имя и тип данных для необязательных аргументов указываются в квадратных скобках.*
Не принимает аргументов.

Возвращаемое значение: *Удалить, если нет значения или this*

Не имеет возвращаемого значения. 
Возвращает объект `this`. 
`{String}`, `{Number}`, `{Array}`, `{Boolean}`, `{Object}`, `{Function}`, `{*}`. В случае если .. –
*Выберите нужное значение.*

<Пример>

<a name="elems-name-declfields"></a>
### Специализированные поля элементов блока

<a name="elems-name-declfields-name"></a>
#### Специализированное поле `название поля` элемента `название элемента`

Тип: `String`, `Number`, `Array`, `Boolean`. *Выберите нужный тип данных.*

<Описание>

<Пример>

<a name="extra-examples"></a>
###Дополнительные примеры
