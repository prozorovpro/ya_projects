# Определение возроста человека на фотографии

---

Сетевой супермаркет «Хлеб-Соль» внедряет систему компьютерного зрения для обработки фотографий покупателей.
Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:
- Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы
- Контролировать добросовестность кассиров при продаже алкоголя.


## Описание набора данных

Данные взяты с сайта [ChaLearn Looking at People](https://chalearnlap.cvc.uab.cat/dataset/26/description/)
В нашем распоряжении одна папка со всеми изображениями (/final_files) и CSV-файл labels.csv с двумя колонками: file_name и real_age. 

## Инструменты

- pandas
- numpy
- matplotlib
- keras
- ResNet50
- ImageDataGenerator
- CNN

## Основные шаги исследования

1. Изучение данных 
2. Построение нейронной сети 
3. Обучение модели 

## Выводы

Для решения задачи была использована RsNet50. использовались предварительно обученные веса для извлечения признаков изображений, добавлнены 3 полносвязных слоя. MAE на валидационной выборке после 50 эпох равна 6,32 что меньше чем требовалось

Модель определяет возраст человека по фото лица, ошибается при этом на 6-7 лет.

- Модель может решить задачу определения возростной группы для предложения товара.
- Для контроля добросовестности кассиров при продаже алкоголя модель не подходит.

## Ссылки

[Ноутбук](https://github.com/prozorovpro/ya_projects/blob/main/%D0%9E%D0%BF%D1%80%D0%B5%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B2%D0%BE%D0%B7%D1%80%D0%BE%D1%81%D1%82%D0%B0%20%D1%87%D0%B5%D0%BB%D0%BE%D0%B2%D0%B5%D0%BA%D0%B0%20%D0%BD%D0%B0%20%D1%84%D0%BE%D1%82%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D0%B8%D0%B8/age_detect.ipynb)