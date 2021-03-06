Вказана таблиця(файл) є довідником версій усіх наявних довідників.

### Структура

Поле   | Обов'язкове |    Тип данних  |   Опис |
:---------------|:--:|:--------------|:--------
**VERSION**  |   |  integer          | Ціле число. Номер версії. Вищий номер - спонукає до оновлення довідника.
**NAME_REF** | √ | varchar(20)       | Найменування довідника. Співпадає з іменем, що починається на IRCG_..., без розширення.



### Зміст

Таблиця містить інформацію про версії довідників, які починаються на `IRCG_...`. Сутність полягає в тому, що всі задіяні організації використовують спільні довідники. Кожна організація має право внести зміни до загального
довідника вказавши номер версії. Якщо номер версії буде найновішим, то цей довідник буде оновлено і його значення будуть використано для всіх.

Тільки певні організації, мають право оновлювати загальні довідники. Наразі це всі організація, які обслуговуються [підприємством “СОФТПРОЕКТ”](http://softproject.com.ua/ua/)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=VERSION;NAME_REF/>
    <Datatypes value=INTEGER;CHARACTER/>
    <Lengths value=8;20/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
