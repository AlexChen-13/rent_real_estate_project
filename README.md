# rent_real_estate_project
  Данный проект реализован в рамках обучения Data Science на Фазе 0 в Elbrus Bootcamp.
  
  **Авторы:** Алексей Ченский и Елизавета Андреева.

  Проект выполняется на основе практической задачи для отдела аналитики и оптимизации международного сервиса по продаже и аренде жилой недвижимости Alyona Ivanovna Real Estate Agency или более известного как AI REA Ltd: 

  - создать модель машинного обучения, которая будет оценивать квартиры и предлагать стоимость аренды максимально похожую на ту, которую выставляют люди 
  - технически задача предполагает улучшить метрику качества модели MAPE с 50% до 30% и менее, т.к. эта метрика показывает среднюю абсолютную ошибку в процентах - очень понятную для менеджеров
    
  Для этого перед нашей группой стоит следующая *задача*:

  Подготовить датасет для разработчиков машинного обучения, используя таблицу с данными исследования рынка аренды квартир в г. Москве, которую выгрузили дата инженеры.

*Подзадачи:*
1. Представить результаты EDA или разведочного анализа данных - Exploratory Data Analysis.
2. Очистить данные от пропусков.
3. Отформатировать исходную таблицу с данными data.csv так, чтобы все значения внутри данных были только численного типа и таблица содержала только уникальные объявления.

## Что было сделано в ходе проекта:

1. На 1 релизе мы произвели первичный анализ, отформатировав некотрые признаки в дата фрейме для возможности построения наиболее наглядных, на наш взгляд, графиков по полученным данным (распределение основных показателей, связь между площадью/количеством комнат и ценой квартиры). Также проанализировали датасет по типам данных в каждой колонке и наличию пропусков в данных. Ноутбук с первичным анализом выгружен в формате html.

2. На 2 релизе было выполнено форматирование названий колонок дата фрейма на английском языке в одно/несколько слов с нижним подчёркиванием. Также мы очистили таблицу от пропусков путем замены пропущенных значений на среднее значение признака (для числовых признаков) или на моду (для категориальных признаков). Результатом стал промежуточный датасет data.csv с внесенными изменениями.

3. На 3 релизе мы отформатировали колонки так, чтобы все значения в таблице было возможно представить в числовом формате. Некоторые колонки, содержащие уникальную для каждого объявления информацию, были удалены, также некоторые колонки были разбиты на несколько, содержащих в себе только один признак. Также мы удалили дубликаты, приняв для сортировки три признака: Address, Price, Additionally. В результате был сформирован итоговый датасет для разработчиков машинного обучения. Процесс обработки данных отражен в файле preprocessing.ipynb.
