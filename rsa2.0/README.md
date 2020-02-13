Справочники и описание изменений для новой версии api
Основные изменения 
1. Использование кода ФИАС вместо кода КЛАДР. 
2. Новый справочник марок и моделей.
3. Изменение в формате запроса. Добавляется поле fias в адресе, марка и модель передаются в тегах <name>, название марки и модели, вместо кодов.

вместо
```html
<model:model>
    <model:vehicleModelCode>1278</model:vehicleModelCode>
    <model:mark>
        <model:vehicleMarkCode>173</model:vehicleMarkCode>
     </model:mark>
 </model:model>
``` 
нужно передавать
```html
<model:model>
    <model:mark>
        <model:name>Nissan</model:name>
     </model:mark>
     <model:name>Note Plus 1</model:name>
 </model:model>
```
Справочник ФИАС можно скачать тут https://fias.nalog.ru/Updates
