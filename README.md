# Geonames
### **Заказчик**

- Карьерный центр Яндекс Практикум

### **Стек:** *pandas, numpy, torch, psycopg2, sqlalchemy, DataLoader, sentence_transformers, NLP*

- ### **Описание проекта**

**Цель:**
:
- Сопоставление произвольных гео названий с унифицированными именами geonames для внутреннего использования Карьерным центр
 
**Задачи:**

- Создать решение для подбора наиболее подходящих названий с geonames. Например Ереван -> Yerevan

- На примере РФ и стран наиболее популярных для релокации - Беларусь, Армения, Казахстан, Кыргызстан, Турция, Сербия. Города с населением от 15000 человек (с возможностью масштабирования на сервере заказчика)


- Возвращаемые поля geonameid, name, region, country, cosine similarity
- формат данных на выходе: список словарей, например [{dict_1}, {dict_2}, …. {dict_n}] где словарь - одна запись с указанными полями



**Задачи опционально:**


- возможность настройки количества выдачи подходящих названий (например в параметрах метода)


- коррекция ошибок и опечаток. Например Моченгорск -> Monchegorsk


- хранение в PostgreSQL данных geonames


- хранение векторизованных промежуточных данных в PostgreSQL


- предусмотреть методы для настройки подключения к БД


- предусмотреть метод для инициализации класса (первичная векторизация geonames)


- предусмотреть методы для добавления векторов новых гео названий


**Результат:** 


- тетрадка с решением задачи (описание проекта, исследование, методы решения)
- python-скрипт, содержащий функцию (класс), для интеграции в систему Заказчиканкцию (класс), для интеграции в систему Заказчикаями
- 
### **Описание данных**
Используемые таблицы с geonames:

- admin1CodesASCII
- alternateNamesV2
- cities15000
- countryInfo
- при необходимости любые другие открытые данные
- таблицы geonames можно скачать здесь http://download.geonames.org/export/dump/
- 
  ### **Вывод**:



ПРОЕКТ в процессе доработки

Планируется:

- Доработка кода, добавить к возврат поле `region`, `country`.
- Доработка python-скрипт, содержащий функцию (класс).
