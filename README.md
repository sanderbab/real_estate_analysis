# Анализ объявлений недвижимости Санкт-Петербурга



В нашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность. 

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма. 


**Цель исследования** 

Установить факторы, от которых зависит стоимость недвижимости. Эти факторы в дальнейшем будут использованы для постороения автоматизированной антимошеннической системы.

**Ход исследования** 

1. Изучим доступные данные.
2. Проверим качество и полноту данных, исправим недочеты в данных, заполним пропуски.
3. Рассчитаем дополнительные столбцы, необходимые для исследования.
4. Проведем исследовательский анализ данных.
5. Сделаем общий вывод.

**Описание данных**

-   `airports_nearest` — расстояние до ближайшего аэропорта в метрах (м)
-   `balcony` — число балконов
-   `ceiling_height` — высота потолков (м)
-   `cityCenters_nearest` — расстояние до центра города (м)
-   `days_exposition` — сколько дней было размещено объявление (от публикации до снятия)
-   `first_day_exposition` — дата публикации
-   `floor` — этаж
-   `floors_total` — всего этажей в доме
-   `is_apartment` — апартаменты (булев тип)
-   `kitchen_area` — площадь кухни в квадратных метрах (м²)
-   `last_price` — цена на момент снятия с публикации
-   `living_area` — жилая площадь в квадратных метрах (м²)
-   `locality_name` — название населённого пункта
-   `open_plan` — свободная планировка (булев тип)
-   `parks_around3000` — число парков в радиусе 3 км
-   `parks_nearest` — расстояние до ближайшего парка (м)
-   `ponds_around3000` — число водоёмов в радиусе 3 км
-   `ponds_nearest` — расстояние до ближайшего водоёма (м)
-   `rooms` — число комнат
-   `studio` — квартира-студия (булев тип)
-   `total_area` — общая площадь квартиры в квадратных метрах (м²)
-   `total_images` — число фотографий квартиры в объявлении