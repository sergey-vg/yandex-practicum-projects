# Исследование объявлений о продаже квартир

## Цель проекта
Для построения автоматизированной системы по отслеживанию мошеннической деятельности нужно определить рыночную стоимость объектов недвижимости. В качестве данных собраны объявления о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет.

## Используемые библиотеки
Для запуска проекта необходимо установить следующие библиотеки:
- pandas
- matplotlib

## Выводы по проекту

***Параметры квартир по всей выборке:***

* Большая часть квартир находится в пределах от 20 до 100 кв. м., больше 200 кв.м. квартир почти нет - редкие выбивающиеся значения
* Стоимость большинства квартир находится в пределах от 1 до 10 млн р., дороже 20 млн. квартир почти нет - редкие выбивающиеся значения
* Большинство квартир 1-3 комнатные, больше 5 комнат - это редкие выбивающиеся значения 
* В большинстве квартир высота потолков находится в пределах от 2,2 до 3,2 м., потолки высотой более 4 м. - это редкие выбивающиеся значения

***Сроки продажи квартир:***

* Обычно продажи занимают от 1 до 200 дней
* Продажи, которые прошли быстрее 30 дней можно считать очень быстрыми, таких продаж менее 25%
* Продажи, которые заняли более года можно считать необычно долгими

***Зависимость цены квартиры от различных параметров, по всей выборке:***

* Цена квартиры сильно зависит от общей площади квартиры (r = 0.73)
* Цена квартиры умеренно зависит от количества комнат в квартире (r = 0.77)
* Цена квартиры умеренно зависит от удаленности квартиры от центра города (r = -0.41)
* Квартиры на первом и последнем этаже стоят дешевле чем квартиры на других этажах, квартиры на первом этаже стоят дешевле всего
* Цена квартиры не зависит линейно от дня недели, месяца или года размещения объявления (|r| < 0,03)
* Кол-во объявлений сильно выросло в 2017 и 2018 год
* В мае меньше всего публикаций объявлений, а в феврале и марте, больше всего
* В выходные дни, публикуется в два раза меньше объявлений, чем в будни

***Границей центральной зоны можно считать расстояние от 0 до 3 км.***

***Сравнительный анализ параметров квартир по центру города и городу в целом:***

* В центре общая площадь квартиры больше, чем в среднем по городу. Медианное значение - 84 кв.м., против 55 кв м.
* В центре стоимость квартир выше, чем в среднем по городу. Медианное значение - 9,5 млн. р., против 5,5 млн. р.
* В центре количество комнат в квартире больше, чем в среднем по городу. Среднее значение - 3,1 комнат, против 2,17 комнат.
* В центре высота потолков в квартирах больше, чем в среднем по городу. Среднее значение - 3,13 м., против 2,77 м.

***Сравнительный анализ  зависимости цены квартиры от различных параметров, по центру города и городу в целом:***

* Цена квартиры сильно зависит от общей площади квартиры, как в центре города (r = 0.63), так и в городе в целом (r = 0.8), но в целом городе, зависимость выражена сильнее, чем в центре города. 
* Цена квартиры умеренно зависит от количества комнат в квартире, как в центре города (r = 0.42), так и в городе в целом (r = 0.51), но в целом городе, зависимость выражена немного сильнее, чем в центре города. 
* Цена квартиры имеет незначительную обратную зависимость (r = -0.11) от удаленности квартиры от центра города, в случае расположения квартиры в границе центра города. В целом по городу, цена квартиры имеет обратную среднею зависимость (r = -0.41) от удаленности квартиры от центра города.
* Цена квартиры умеренно зависит от площади кухни, как в центре города (r = 0.38), так и в городе в целом (r = 0.51), но в целом городе, зависимость выражена сильнее, чем в центре города.
* Цена квартиры умеренно зависит от общей жилой площади в квартире, как в центре города (r = 0.58), так и в городе в целом (r = 0.6).
* В целом по городу, цена квартиры имеет маленькую завимость (r = 0.2) от количества водоёмов в радиусе 3 км., а в центре города, зависимоть отсутствует совсем (r = -0.012).