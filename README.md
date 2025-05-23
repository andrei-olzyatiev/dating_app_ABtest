#   A/B тестирование изменения стоимости премиум-подписки
##  Описание проекта
Этот проект представляет анализ результатов A/B тестирования, проведенного в крупном дейтинговом приложении. Цель теста состояла в проверке влияния изменения стоимости премиум-подписки на поведение пользователей, их платежеспособность и выручку компании. Тест затрагивал новых пользователей из нескольких стран и предусматривал использование двух новых платежных систем.

##  Проект включает:
-   Загрузку и предобработку данных пользователей и транзакций.
-   Выделение ключевых метрик для оценки результата теста:
    -   ARPPU (Average Revenue Per Paying User) — средний доход с платного пользователя.
    -   CR (Conversion Rate) — конверсия из пробных подписок в платные.
-   Анализ поведения пользователей по различным категориям:
    -   Гендер, возраст, коэффициент привлекательности.
    -   Страны, откуда пользователи пришли.
    -   Частота и длительность посещения приложения.
-   A/B тестирование с использованием статистических методов:
    -   Тесты на нормальность распределения и равенство дисперсий.
    -   Использование t-теста, хи-квадрат теста и бутстреп-методов для проверки гипотез.

##  Выводы по анализу сегментов пользователей
Изменение стоимости премиум-подписки способствовало изменению следующих метрик.
+ **Для пользователей до 30 лет включительно**:
   + Отсутствие изменений ARPPU
   + Уменьшение конверсии в премиум подписку на 55%
+ **Для пользователей старше 30 лет**:
   + Отсутствие изменений ARPPU
   + Отсутствие изменения конверсии
+ **Для пользователей из развивающихся стран**:
   + Отсутствие значимого изменения ARPPU
   + Отсутствие значимого изменения конверсии
+ **Для пользователей из развитых стран**:
   + Отсутствие значимого изменения ARPPU
   + Уменьшение конверсии на 62.5%

##  Итоговые выводы и рекомендации
Увеличение стоимости премиум-подписки не изменило средний доход с платящего пользователя и конверсию в премиум-подписку. При этом, в некоторых сегментах (пользователи до 30 лет, пользователи из развитых стран) конверсия в премиум подписку снизилась более чем на 50%, что способствует уменьшению общей выручки. Следовательно, изменение стоимости премиум-подписки не рекомендуется.

##  Структура данных
### Файлы:
    -   users_*.csv — информация о пользователях (демография, активность, премиум-статус).
    -   transactions_*.csv — информация о платежах (выручка, тип подписки, источник оплаты).
### Основные столбцы:
    -   uid — идентификатор пользователя.
    -   age, gender, attraction_coeff — характеристики пользователя.
    -   was_premium, is_premium — статус премиум-подписки.
    -   revenue, total_revenue — нормированная выручка.
    -   product_type — тип продукта (пробная или постоянная подписка).

##  Используемые библиотеки
Проект реализован на Python с использованием следующих библиотек:
-   Pandas, NumPy — работа с данными.
-   Matplotlib, Seaborn, Plotly — визуализация.
-   Scipy, Statsmodels, Pingouin — статистический анализ.
-   Bootstrap — оценка доверительных интервалов.
##  Как использовать
1.  Скачайте данные с указанных источников (например, облачное хранилище).
2.  Выполните предобработку данных, следуя коду в проекте.
3.  Проведите анализ ключевых метрик и A/B тестирование.
4.  Используйте результаты для принятия решений по ценообразованию в приложении.
