# Разведочный анализ данных с продажами в магазинах Эквадора

### Данные

В исследовании используются данные с продажами различных продуктов в магазинах Эквадора. Данные включают в себя информацию о магазине и продукте, о том, рекламировался ли товар, а также объем продаж.

Данные можно найти по ссылке: https://www.kaggle.com/competitions/store-sales-time-series-forecasting.

**Используемые файлы**
```
- train_df.csv - the training set. Daily historical data from January 2013 to October 2015.
- stores.csv - the test set. You need to forecast the sales for these shops and products for November 2015.
- oil.csv
- holiday_events.csv
```

**Описание данных**
```
- ID - an Id that represents a (Shop, Item) tuple within the test set
- shop_id - unique identifier of a shop
- item_id - unique identifier of a product
- item_category_id - unique identifier of item category
- item_cnt_day - number of products sold. You are predicting a monthly amount of this measure
- item_price - current price of an item
- date - date in format dd/mm/yyyy
- date_block_num - a consecutive month number, used for convenience. January 2013 is 0, February 2013 is 1,..., October 2015 is 33
- item_name - name of item
- shop_name - name of shop
- item_category_name - name of item category
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
![Ipynb](https://img.shields.io/badge/Python-matplotlib-blue.svg?style=flat&logo=python&logoColor=white) 
![Ipynb](https://img.shields.io/badge/Python-seaborn-blue.svg?style=flat&logo=python&logoColor=white)
![Ipynb](https://img.shields.io/badge/Python-scipy-blue.svg?style=flat&logo=python&logoColor=white) 
![Ipynb](https://img.shields.io/badge/Python-sklearn-blue.svg?style=flat&logo=python&logoColor=white) 
