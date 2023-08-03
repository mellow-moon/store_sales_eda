# Разведочный анализ данных с продажами в магазинах Эквадора

## Данные

В исследовании используются данные с продажами различных продуктов в магазинах Эквадора. Данные включают в себя информацию о магазине, продукте, о том, рекламировался ли товар, а также объем продаж.

Данные можно найти по ссылке: https://www.kaggle.com/competitions/store-sales-time-series-forecasting.

## Используемые файлы
```
- train_df.csv - объем продаж
- stores.csv - информация о магазинах
- oil.csv - ежедневные показатели цен на нефть
- holiday_events.csv - праздники и прочие события
```

### Описание данных

### train_df.csv

```
- store_nbr - номер магазина, в котором был продан продукт
- family - тип проданного продукта
- sales - объем продаж определенного продукта в определенном магазине в указанный день
- onpromotion - число рекламируемых товаров определенного типа в указанный день
```

### stores.csv

```
- city - город
- state - штат
- type - тип магазина
- cluster - кластер (схожие магазины образуют общий кластер)
```

### oil.csv

```
- date - дата
- dcoilwtico - цена на нефть
```

### holiday_events.csv

```
- date - дата
- type - тип (праздник Holiday либо событие Event)
- locale - является ли праздник национальным или региональным
- locale_name - имя региона
- description - описание праздника или события
- transferred - был ли праздник перенесен
```

### Исследуемые вопросы

1. Какая доля продаж приходится на каждый тип продукта? У каких продуктов продажи больше и у каких меньше?
2. Какая доля продаж приходится на каждый магазин? В каких магазинах наибольший объем продаж? Что это за магазины?
3. Влияет ли тип магазина на объем продаж?
4. Какая доля продаж приходится на каждый штат?
5. Оказывают ли цены на нефть влияние на объем продаж?
6. В каком городе наибольшее количество клиентов?
7. В каком штате наибольшее количество клиентов?
8. В каких месяцах продажи были наибольшими и наименьшими?

### Используемые библиотеки

![Ipynb](https://img.shields.io/badge/Python-pandas-blue.svg?style=flat&logo=python&logoColor=white)
![Ipynb](https://img.shields.io/badge/Python-numpy-blue.svg?style=flat&logo=python&logoColor=white)
![Ipynb](https://img.shields.io/badge/Python-plotly-blue.svg?style=flat&logo=python&logoColor=white)
![Ipynb](https://img.shields.io/badge/Python-scipy-blue.svg?style=flat&logo=python&logoColor=white)

# Выводы

1. Доли продаж распределены не равномерно. Наибольшую долю занимают Товары первой необходимости (32%), Напитки (20%) и Сельскохозяйственная продукция (11%). Наименьшую - Книги (<1%), Уход за детьми (<1%), Бытовая техника (<1%).

2. Наибольшая доля продаж приходится на магазины 44 (5.78%), 45 (5.08%) и 47 (4.75%). Большинство магазинов с лучшими продажами находятся в городе Quito, при этом среди лучших магазинов наиболее часто встречаются магазины типа A. Из 10 магазинов с самыми низкими продажами 4 находятся в городе Guayaquil. Половина магазинов с низкими продажами имеют тип C.

3. По результатам дисперсионного анализа можно сделать вывод, что тип магазина влияет на объем продаж.

4. Доли продаж по каждому штату распределены не равномерно. Наибольшую долю занимают штаты Pichincha (54%), Guayas (15%) и Azuay (5%).

5. В данных присутствует отрицательная корреляция между ценами на нефть и суммарным объемом продаж.

6. Наибольший объем продаж был зафиксирован в городе Quito, можно сделать вывод, что наибольшее количество клиентов проживает в этом городе.

7. Наибольший объем продаж среди всех штатов показал штат Pichincha, это позволяет сделать вывод, что в этом штате проживает наибольшее количество клиентов.

8. Рекорд по продажам был установлен в декабре 2016 года. Декабрь - это самый доходный месяц в году (кроме 2017 года, так как данные о продажах в этом году были собраны только до августа). С каждым годом объем продаж увеличивается. В 2014 году есть два месяца с аномально высокими продажами. В июне 2015 года произошел сильный рост продаж, затем рост продолжился, но уже более медленными темпами.
