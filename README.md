Проект 6. Car Price Prediction Прогнозирование стоимости автомобиля по характеристикам: DST-PRO Профессия Data Scientist

slack: Aleksandr_N  member ID: U01B1CP7YVC

ЗАДАЧА:
https://www.kaggle.com/c/sf-dst-car-price-prediction
Вы работаете в компании, которая занимается продажей автомобилей с пробегом в Москве. 
Основная задача компании и её менеджеров — максимально быстро находить выгодные предложения (проще говоря, купить ниже рынка, а продать дороже рынка). 
Руководство компании просит вашу команду создать модель, которая будет предсказывать стоимость автомобиля по его характеристикам.
Если такая модель будет работать хорошо, то вы сможете быстро выявлять выгодные предложения (когда желаемая цена продавца ниже предсказанной рыночной цены). Это значительно ускорит работу менеджеров и повысит прибыль компании.

ПРОБЛЕМА:
Только вот незадача: исторически сложилось, что компания изначально не собирала данные. Есть только небольшой датасет с историей продаж за короткий период, которого для обучения модели будет явно мало. Его мы будем использовать для теста, остальное придется собрать самим.

КОМАНДА на kaggle: new_new_team49: AleksandrNisch, Makcimilian, Olga Markhai. Моя первая работа в команде над проектом.
https://www.kaggle.com/makcimilian
https://www.kaggle.com/olgamarkhai

Участие в ХАКАТОНЕ: https://www.kaggle.com/olgamarkhai/new-new-team49?scriptVersionId=85523032
Используемые датасеты: https://disk.yandex.ru/d/uxvpQ3mpQ8X8IA

Этапы проекта:
- Парсинг;
- EDA, Предобработка;
- Обработка пропусков;
- Визуализация данных;
- Оценка корреляций;
- Оценка значимости непрерывных переменных;
- Обработка категориальных переменных;
- Обработка выбросов;
- Отбор признаков для моделирования;
- Подготовка данных к машинному обучению;
- Предварительный анализ ML;
- Выбор модели.

Выводы
Новые признаки:
HAS_OPTION_isofix - был создан на основе информации в признаке complectation_dict
HAS_OPTION_wheel-leather - был создан на основе информации в признаке complectation_dict
Результаты моделирования:
Модель #1 - Наивная модель
Модель №2: CatBoost
Точность модели по метрике MAPE без логтаргета: 13.12% Точность модели по метрике MAPE с логтаргетом: 11.81%
Модель 3: RandomForestRegressor
Точность модели по метрике MAPE без логтаргета: 12.95% Точность модели по метрике MAPE с логтаргетом: 12.16% Точность модели по метрике MAPE с логтаргетом и гиперпараметрами: 12.07%
Модель 4: XGBRegressor
Точность модели по метрике MAPE без логтаргета: 13.54% Точность модели по метрике MAPE с логтаргетом: 11.99% Точность модели по метрике MAPE с логтаргетом и max_depth=8: 11.89%
Модель 5: ExtraTreesRegressor
Точность модели по метрике MAPE без логтаргета: 12.04% Точность модели по метрике MAPE с логтаргетом: 12.31%
Модель 6: BaggingRegressor
RandomForest Точность модели по метрике MAPE с логтаргетом: 12.25%
ExtraTreesRegressor Точность модели по метрике MAPE с логтаргетом: 12.04%
Модель 7. StackingRegressor
Xgboosting, ExtraTreesRegressor+LinearRegression Точность модели по метрике MAPE: 11.81%
Xgboosting, ExtraTreesRegressor+CatBoostRegressor Точность модели по метрике MAPE: 12.22%
RandomForestRegressor, ExtraTreesRegressor+LinearRegression Точность модели по метрике MAPE: 12.03%
BaggingRegressor(xgb.XGBRegressor), ExtraTreesRegressor+LinearRegression Точность модели по метрике MAPE: 11.70%
BaggingRegressor(ExtraTreesRegressor), ExtraTreesRegressor+LinearRegression Точность модели по метрике MAPE: 12.05%

Лучшая модель:
BaggingRegressor: xgb.XGBRegressor,ExtraTreesRegressor+LinearRegression Точность модели по метрике MAPE: 11.65%

Благодарность студентам, ранее закончившм проект у которых, я смержил часть кода и моим соисполнителям за их труд! 
Далее можно поискать лучшие сочетания параметров и моеделей и подняться в рейтинге.
