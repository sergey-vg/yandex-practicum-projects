# Дипломный проект. Прогнозирование температуры стали

## Цель проекта
С целью оптимизации производственных расходов металлургический комбинат решил уменьшить потребление электроэнергии на этапе обработки стали. Необходимо построить модель, которая будет предсказывать температуру стали.

## Используемые библиотеки
Для запуска проекта необходимо установить следующие библиотеки:

* lightgbm
* matplotlib
* numpy
* optuna
* pandas
* seaborn
* tensorflow
* keras
* sklearn
* sqlalchemy

## Что было сделано
* подключился к базе данных и выполнил первичное исследование таблиц;
* провёл детальное исследование всех признаков во всех таблицах, обработал аномальные значения (в случаях, когда это было необходимо);
* с помощью статистического анализа нашёл закономерности в данных и некоторые несоответствия;
* добавил новые признаки;
* объединил все таблицы в единый датасет и обработал пропуски;
* разделил данные на выборки и отмасштабировал количественные признаки;
* подобрал гиперпараметры с помощью Optuna;
* обучил три моделей регрессии, в том числе полносвязную нейронную сеть;
* исследовал важность признаков для лучшей модели и построил графики зависимости. 

## Итоговые результаты
* Результаты моделей на валидационных данных:
    * Модель полносвязной нейронной сети показала лучший результат - 5.71, но её результаты нестабильны, происходят сильные колебания;
    * Модель CatBoostRegressor показала близкий результат - 5.77 (MAE), что гораздо ниже заданого таргета - 6.3 и при этом её результаты весьма стабильны, поэтому остановил свой выбор на данной модели;
    * Модель RandomForestRegressor показала наихудший результат - 6.26, но данный показатель все равно ниже заданного таргета.
* CatBoostRegressor показала отличный результат на тестовых данных - 5.16 (MAE), гораздо ниже заданого таргета - 6.3.
* Самым важным признаком для модели CatBoostRegressor, является суммарное время нагрева - при увеличении времени нагрева, увеличивается и итоговая температура.