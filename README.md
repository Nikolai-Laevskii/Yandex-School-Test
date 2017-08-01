# Yandex School Test

## Валидация полей

Так как для валидации полей используются регулярные выражения, которые сами по себе не очень легко читаемые и довольно длинные, наверное, следует описать что же они делают.

### Правила валидации ФИО

В задании требовалось создать поле для ввода ФИО. 
Имена такого формата встречаются преимущественно на территории СНГ, в связи с этим, а так же с тем, что подобные формы как правило предполагают запись имени с помощью символов алфавита какого-то конкретного языка и что имена никогда не записываются символами из разных алфавитов, разработка велась исходя из предположения, что ФИО должно быть записано с помощью букв русского алфавита.

Подтверждение ФИО происходит по следующим правилам:
1. Ровно три слова
2. Каждое слово может содержать в себе буквы русского алфавита, а так же символы апострофа (' или ’‎) и дефиса (-)
3. Слово не может начинаться с апострофа или дефиса
4. Слово не может заканчиваться апострофом или дефисом
5. Символы, не являющиеся буквами (апострофы и дефисы), не могут идти подряд
6. Вокруг слов может быть произвольное количество пробелов

Ограничений на количество букв не накладывалось. В теории слово, в том числе и Имя/Фамилия/Отчество может состоять из одной буквы.

Примеры:

Иванов Иван Иванович, Иванов-Петров Иван Иванович, Д’Артаньян Иван Иванович — пройдут валидацию;

Иванов--Петров Иван Иванович, --Иванов-- Иван Иванович, ' ' ', - - -, Иванов Иван — не пройдут валидацию.

### Правила валидации Email

Подтверждение Email происходит по следующим правилам:
1. Может содержать в себе буквы латинского алфавита, цифры и символы точки (.) и дефиса (-)
2. Не может начинаться с точки или дефиса
3. Не может начинаться с цифры
4. Не может заканчиваться точкой или дефисом
5. Символы, не являющиеся буквами (точки и дефисы), не могут идти подряд
6. Оканчиваться может только на @ya.ru, @yandex.ru, @yandex.ua, @yandex.by, @yandex.kz или @yandex.com
7. Максимальное количество символов до @ — 30

Правила составлены исходя из соответствующих ограничений в сервисах Яндекс

Примеры:

ya@ya.ru, henry-ford@yandex.by, henry.ford@yandex.kz, henryford63@yandex.ua, henry-fordhenry-fordhenry-ford@yandex.ru — пройдут валидацию;

ya.ru, @ya.ru, henry---ford@yandex.by, .henry.ford@yandex.kz, 63henryford@yandex.ua, henry.-ford@ya.ru, henry-fordhenry-fordhenry-ford1@yandex.ru — не пройдут валидацию.

### Правила валидации телефона

Подтверждение телефона происходит по следующим правилам:
1. Должен соответствовать шаблону +7(XXX)XXX-XX-XX
2. Сумма всех цифр не может превышать 30


##### Примечания

Страница как надо отображается в последних версиях Chrome, Opera, Edge и Яндекс.Браузер.
Есть небольшие проблемы с отображением в Firefox.
Есть большие проблемы с отображением в Internet Explorer.

Корректная работа скрипта только в браузерах, поддерживающих синтаксис ES6.
