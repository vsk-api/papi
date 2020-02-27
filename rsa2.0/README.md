Справочники и описание изменений для новой версии api
Основные изменения 
1. Использование кода ФИАС вместо кода КЛАДР. 
2. Новый справочник марок и моделей.
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
