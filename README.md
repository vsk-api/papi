1. API eOSAGO - Спецификация интерфейса API eOSAGO

2. СправочникАвто - Справочник марок и моделей ТС

3. main_process - Диаграмма процесса Part API

История изменений: 

14.08.2019 Обновлен файл до версии 1.0.6. Ключевые изменения: Обновлена ссылка вызова параметра SavePolicy (Save - с большой буквы). 
Изменено форматирование текста. 

20.09.2019 Обновлен файл до версии 1.0.7. Ключевые изменения: Обновлена ссылка вызова параметра BuyPolicy (Buy - с большой буквы). 

06.11.2019 Добавлен список ошибок валидации

07.11.2019 v.1.1.1. Добавлена информация о телеграмм канале

01.06.2020 v.2.0.0. РСА 2.0

Основные изменения 
1. Использование кода ФИАС вместо кода КЛАДР. Передаваемые значения ФИАС должны быть 6го уровня или выше.
2. Новый справочник марок и моделей. ( models.csv )
3. Изменения в кодировке категорий авто. ( стправочник ТипыТС.csv )
3. Изменение в формате запроса. Добавляется поле fias в адресе, марка и модель передаются в тегах <name>, название марки и модели, вместо кодов.

вместо
```html
<model:policyObjects>
...
    <model:model>
        <model:vehicleModelCode>1278</model:vehicleModelCode>
        <model:mark>
            <model:vehicleMarkCode>173</model:vehicleMarkCode>
        </model:mark>
        <model:type>
             <model:vehicleTypeCode>B</model:vehicleTypeCode>
        </model:type>
    </model:model>
...
    <model:power>150</model:power>
    <model:yearIssue>2005</model:yearIssue>
... 
</model:policyObjects>
``` 
нужно передавать
```html
<model:policyObjects>
...
    <model:model>
         <model:mark>
             <model:name>Nissan</model:name>
         </model:mark>
         <model:type>
             <model:vehicleTypeCode>B</model:vehicleTypeCode>
         </model:type>
         <model:name>Note Plus 1</model:name>
     </model:model>
...
    <model:power>150</model:power>
    <model:yearIssue>2005</model:yearIssue>
... 
</model:policyObjects>
```
Справочник ФИАС можно скачать тут https://fias.nalog.ru/Updates

```xml
<model:addresses>
    <model:country>
        <model:countryCode>Россия</model:countryCode>
    </model:country>
    <model:addressType>
        <model:addressTypeCode>REGISTRATION</model:addressTypeCode>
    </model:addressType>
    <model:region/>
    <model:district/>
    <model:city>Москва</model:city>
    <model:locality/>
    <model:street>Островная Улица</model:street>
    <model:house>16</model:house>
    <model:building>1</model:building>
    <model:flat>119</model:flat>
    <model:okato/>
    <model:addressStr/>    
    <model:kladr>77000000000</model:kladr>
    <model:fias>77000000000</model:fias> 
</model:addresses>
```    

21.08.2020 v 2.1 Изменение тарифа ОСАГО
Добавлено 
  1. Семейное положение для владельца авто 
  2. IP адрес страхователя
