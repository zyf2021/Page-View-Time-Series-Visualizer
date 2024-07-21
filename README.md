# Page-View-Time-Series-Visualizer
Для этого проекта была проведена визуализация временных рядов с использованием линейного графика, столбчатой диаграммы и коробчатых диаграмм. Визуализация выполнена с помощью библиотек Pandas, Matplotlib и Seaborn, на основе набора данных, содержащего количество просмотров страниц каждый день на форуме freeCodeCamp.org за период с 2016-05-09 по 2019-12-03. Визуализация данных позволила выявить закономерности посещений и определить годовой и месячный рост.

### Выполненные задачи:

1. **Импорт данных**: Данные из "fcc-forum-pageviews.csv" были импортированы с помощью Pandas. Индекс был установлен по столбцу с датами.
2. **Очистка данных**: Дни с количеством просмотров страниц в верхних 2.5% и нижних 2.5% набора данных были отфильтрованы для очистки данных.
3. **Линейный график**: 
   - Создана функция `draw_line_plot`, которая с помощью Matplotlib построила линейный график, аналогичный "examples/Figure_1.png".
   - Заголовок графика: "Daily freeCodeCamp Forum Page Views 5/2016-12/2019".
   - Метка на оси x: "Date", метка на оси y: "Page Views".
4. **Столбчатая диаграмма**: 
   - Создана функция `draw_bar_plot`, которая построила столбчатую диаграмму, аналогичную "examples/Figure_2.png".
   - Диаграмма показывает среднее количество ежедневных просмотров страниц для каждого месяца, сгруппированных по годам.
   - Легенда содержит метки месяцев с заголовком "Months".
   - Метка на оси x: "Years", метка на оси y: "Average Page Views".
5. **Коробчатые диаграммы**: 
   - Создана функция `draw_box_plot`, которая с помощью Seaborn построила две смежные коробчатые диаграммы, аналогичные "examples/Figure_3.png".
   - Диаграммы показывают, как значения распределяются в течение года или месяца и как они меняются со временем.
   - Заголовок первого графика: "Year-wise Box Plot (Trend)", заголовок второго графика: "Month-wise Box Plot (Seasonality)".
   - Метки месяцев внизу начинаются с января, оси x и y правильно подписаны.

### Разработка и тестирование
- Весь код проекта написан в файле `time_series_visualizer.py`.
- Для тестирования использовался файл `main.py`.
- Модульные тесты находятся в файле `test_module.py` и были импортированы в `main.py` для удобства.
