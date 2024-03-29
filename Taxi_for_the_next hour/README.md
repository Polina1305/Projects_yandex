# Прогнозирование заказов такси

|Статус проекта:|	В плане 🔲|	Выполняется 🔲|	Завершён ✅|
|---------------|-----------|----------------|-------------|

На основании данных о заказах такси в аэропортах спрогнозировала количество заказов такси на следующий час.

## Использованные библиотеки: 
 - pandas
 - sklearn
 - numpy
 - statsmodels,
 - matplotlib 
 - catboost
 - lightgbm

## Подготовка данных
Данные загружены, просмотренны. Пропусков нет, временной ряд монотонный. Проведенно ресемплирование данных по 1 часу.

## Анализ данных
В результате анализа получены следующие результаты: в целом идет увеличение числа заказов - это может быть связано с тем, что летом люди чаще летают в отпуск, а может быть и в целом с увеличением популярности приложения. Сезонности нет - опять же небольшой промежуток времени, но интересно, что нет изменения спроса по выходным, например.

## Обучение моделей
Построены 4 модели - линейная регрессия, CatBoost, LightGBM и RandomForest. Для оценки качества использовалась метрика RMSE. На валидационной выборке лучше всего себя показала Линейная регрессия, поэтому эта модель выбрана для тестирования.

По итогу проведённой работы мы выбрали перспективную модель CatBoost для прогнозирования количества заказов такси на следующий час.

## Тестирование
На тестовых данных результат RMSE = 43,78.
