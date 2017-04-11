# 1C-configuration

## Возможности

* Обмен заказами 
* Выгрузка каталога
* Выгрузка цен и остатков
* В модуле 1Cv8_Intaro_8.3_УТ11.cf добавлена возможно выгрузки типов цен

## Объекты интеграции

### В модуле 1Cv8_intaro_8.2: 

* Общий модуль - Интаро_общий
* Подписка на событие - Интаро_документы
* Константа - Интаро_константы
* Обработка - IntaroШаблонноеРешение


### В модуле 1Cv8_Intaro_8.3_УТ11: 

* Подсистема - RetailCRMИнтеграция
* Общий модуль - RetailCRM_Общий
* Роль - RetailCRMИнтеграция
* Общие картинки - RetailCRM и RetailCRMlogo
* Подписка на событие - RetailCRM_документы
* Константа - RetailCRM_константы
* Обработка - RetailCRMШаблонноеРешение


## Порядок интеграции

* Добавляем объекты в конфигурацию
* С помощью обработки инициализируем константы, сохраняем.
* С помощью обработки выполняется загрузка заказов из retailCRM, выгрузка остатков и цен в retailCRM, выгрузка типов цен (если используются) и если есть необходимость то и выгрузка каталога номенклатуры в retailCRM.
* Выгрузка данных по заказу из 1С в retailCRM происходит при проведении заказа.
* Для этих целей и нужна подписка на событие. Её настраиваем под нужную конфигурацию.
* Для автоматической загрузки заказов настраивается регламентное задание.
* Подробное описание настройки можно посмотреть по ссылке: [http://www.retailcrm.ru/docs/Users/1C](http://www.retailcrm.ru/docs/Users/1C)
