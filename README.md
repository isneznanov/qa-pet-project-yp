# QA Engineer Portfolio | Учебные проекты по тестированию

Привет! Меня зовут **Илья Незнанов**, я QA-инженер (ручное тестирование). В этом репозитории собраны проекты, которые я выполнил на курсе «Инженер по тестированию» (Яндекс Практикум): тестовая документация, баг-репорты, отчёты и запросы.

Проекты охватывают **Web**, **Mobile (Android)**, **REST/SOAP API** и **SQL**.

---

## Кратко о проектах

| # | Проект | Тип | Что сделано | Артефакты |
|:-:|:--|:--|:--|:--|
| 1 | [Яндекс.Маршруты: формы и расчёты](#1-web-яндексмаршруты-тестирование-форм-и-расчётов) | Web, функциональное | Тест-кейсы на валидацию и расчёты, баг-репорты | Excel |
| 2 | [Яндекс.Маршруты: каршеринг](#2-web-яндексмаршруты-каршеринг) | Web, UI + функциональное | Чек-листы на вёрстку и логику, тест-кейсы, баг-репорты | Excel |
| 3 | [Яндекс.Метро](#3-mobile-яндексметро-android) | Mobile, функциональное + регресс | Чек-листы, тестирование в Android Studio, баг-репорты | Excel, настройка эмулятора |
| 4 | [Яндекс.Прилавок](#4-api-яндексприлавок) | API (REST + SOAP/XML) | Чек-лист, тестирование в Postman, баг-репорты | Excel, запросы Postman |
| 5 | [Анализ данных на SQL](#5-sql-анализ-данных-о-фондах-и-инвестициях) | SQL | 8 задач и запросы к ним | SQL-запросы |

**Технологии и инструменты:**
`Postman` `Charles Proxy` `DevTools` `Android Studio` `ADB` `Figma` `YouTrack` `Swagger / Apidoc` `SQL (PostgreSQL)` `JSON / XML` `Google Sheets / Excel`

**Техники тест-дизайна:** классы эквивалентности, граничные значения, таблицы принятия решений, попарное тестирование, позитивные и негативные проверки.

---

## 1. Web. Яндекс.Маршруты: тестирование форм и расчётов

**О продукте:** сервис строит маршруты для разных видов транспорта и рассчитывает время и стоимость поездки.

**Задача:** подготовить тестовый набор и протестировать на стенде:
- валидацию полей ввода времени и адресов;
- логику расчёта времени и стоимости поездки на собственном автомобиле (20 руб. за 1 км, скорость и расстояния по таблицам из требований).

**Что я делал:**
- провёл тест-анализ требований, нашёл серые зоны и уточнил их;
- спроектировал тест-кейсы с помощью классов эквивалентности и граничных значений;
- выполнил тестирование на стенде и оформил баг-репорты;
- подготовил отчёт о проделанной работе.

**Результат:** <!-- Например: N тест-кейсов, найдено N багов (из них N критичных) -->

**Артефакты:**
- 📊 Рабочая таблица: [смотреть онлайн](https://docs.google.com/spreadsheets/d/16XVMzdmNyN7uJyT88o_9JJCvbuDsaPg3/edit?usp=sharing&ouid=104910583496811000029&rtpof=true&sd=true) | [скачать .xlsx](https://github.com/isneznanov/qa-pet-project-yp/blob/main/01_Web_Routes_Forms.xlsx)

---

## 2. Web. Яндекс.Маршруты: каршеринг

**Задача:** протестировать новый функционал каршеринга: подготовить тестовую документацию, выполнить проверки, завести баг-репорты, подготовить отчёт. Тариф для тестирования: «Походный».

**Что я делал:**
- составил **чек-лист на вёрстку** формы бронирования и элементов навигационной карты (иконки автомобилей и действия с ними) по макетам Figma и требованиям;
- составил **чек-лист на логику** окон «Способ оплаты» и «Добавление карты»;
- написал **тест-кейсы** на кнопку «Забронировать»;
- протестировал приложение по своей документации и завёл баг-репорты в YouTrack;
- проверил новый функционал, реализованный только на фронтенде, с подменой ответа сервера в Charles;
- подготовил отчёт о тестировании.

**Результат:** <!-- Например: N проверок в чек-листах, N тест-кейсов, найдено N багов, из них N блокирующих -->

**Артефакты:**
- 📊 Рабочая таблица: [смотреть онлайн](https://docs.google.com/spreadsheets/d/1JIqrSli-S7Z8BN_SNyDpERaEnlBtsr4t/edit?usp=sharing&ouid=104910583496811000029&rtpof=true&sd=true) | [скачать .xlsx](https://github.com/isneznanov/qa-pet-project-yp/blob/main/02_Web_Carsharing.xlsx)

---

## 3. Mobile. Яндекс.Метро (Android)

**Задача:** после рефакторинга приложения проверить изменённые части, провести регрессионное тестирование и определить, можно ли выпускать новую версию в стор.

**Окружение:**

| Параметр | Значение |
|:--|:--|
| Приложение | Яндекс.Метро, сборка v3.6 (предыдущая версия: v2.13) |
| Инструмент | Android Studio, эмулятор (Virtual Device) |
| Устройство | Honor 8, 5.5", 1080×1920 |
| ОС | Android 9.0 Pie |

**Что я делал:**
- настроил тестовое окружение: Android Studio, Virtual Device, установка сборки из APK;
- составил **чек-лист функционального тестирования** для требований, которые затронул рефакторинг;
- составил **чек-лист регрессионного тестирования** с учётом мобильной специфики: взаимодействие с устройством, прерывания, обновление приложения, работа сети и т. д.;
- выполнил тестирование, при необходимости снимал логи (Logcat / ADB);
- оформил баг-репорты и отчёт.

**Результат:** <!-- Например: N проверок, найдено N багов, рекомендация по релизу -->

**Артефакты:**
- 📊 Рабочая таблица: [смотреть онлайн](https://docs.google.com/spreadsheets/d/13nlE47Rto7BuJdN-Yq4UZ24rre1D_zun/edit?usp=sharing&ouid=104910583496811000029&rtpof=true&sd=true) | [скачать .xlsx](https://github.com/isneznanov/qa-pet-project-yp/blob/main/03_Mobile_Metro.xlsx)
- 🛠️ [Настройка эмулятора в Android Studio](https://github.com/isneznanov/qa-pet-project-yp/blob/main/additional_materials/Configure_virtual_device.pdf)

---

## 4. API. Яндекс.Прилавок

**Задача:** протестировать новую функциональность бэкенда: спроектировать тесты, проверить API через Postman, завести баг-репорты, написать отчёт. Авторизация в объём тестирования не входила.

**Тестируемые ручки:**

| Метод | Ручка | Назначение |
|:--|:--|:--|
| `POST` | `/api/v1/kits/{id}/products` | Добавление продуктов в набор |
| `POST` | `/fast-delivery/v3.1.1/calculate-delivery.xml` | Проверка доставки курьерской службой и её стоимости (XML) |
| `GET` | `/api/v1/orders/:id` | Получение списка продуктов в корзине |
| `PUT` | `/api/v1/orders/:id` | Добавление продуктов в корзину |
| `DELETE` | `/api/v1/orders/:id` | Удаление корзины |

**Что я делал:**
- проанализировал требования к бэкенду и к расчёту доставки, изучил документацию в Apidoc;
- спроектировал чек-лист (позитивные и негативные проверки, классы эквивалентности, граничные значения);
- выполнил проверки в Postman: статус-коды, структура и содержимое ответа, обработка некорректных данных;
- оформил баг-репорты и отчёт о тестировании.

**Результат:** <!-- Например: N проверок, найдено N багов, ключевые находки -->

**Примеры запросов Postman:**

<!-- Вставьте по одному примеру на каждый метод. Остальные запросы отличаются только параметром (например, id 1, 4, 5, 6, 10). -->

<details>
<summary><b>POST</b> добавление продуктов в набор</summary>

```cURL
curl --location 'https://***.serverhub.praktikum-services.ru/api/v1/kits/3/products' \
--header 'Content-Type: application/json' \
--data '{
    "productsList": [
        {
            "id": 2,
            "quantity": 2
        }
    ]
}'
```
</details>

<details>
<summary><b>PUT</b> добавление продуктов в корзину</summary>

```cURL
curl --location --request PUT 'https://***.serverhub.praktikum-services.ru/api/v1/orders/3/products' \
--header 'Authorization: 16586ac5-4578-48a8-936c-ecd9af4acbb9' \
--header 'Content-Type: application/json' \
--data '{"productsList": [{"id": 35, "quantity": 1}]}'
```
</details>

**Артефакты:**
- 📊 Рабочая таблица: [смотреть онлайн](https://docs.google.com/spreadsheets/d/1BTyhiSWYNuJjrufgWKqwbm7_RgfkBwiE/edit?usp=sharing&ouid=104910583496811000029&rtpof=true&sd=true) | [скачать .xlsx](https://github.com/isneznanov/qa-pet-project-yp/blob/main/04_API_Prilavok.xlsx)

---

## 5. SQL. Анализ данных о фондах и инвестициях

**Задача:** проанализировать данные о компаниях, людях, фондах и инвестициях и написать запросы к базе (PostgreSQL).

**Навыки:** `WHERE`, `LIKE`, `BETWEEN`, `GROUP BY`, `HAVING`, `ORDER BY`, `LIMIT`, `LEFT JOIN`, агрегирующие функции, работа с датами.

![ER-диаграмма](https://github.com/isneznanov/qa-pet-project-yp/blob/main/additional_materials/basic_sql_project.png)
[Описание ER-диаграммы](https://github.com/isneznanov/qa-pet-project-yp/blob/main/additional_materials/basic_sql_project.pdf)

**1. Посчитать, сколько компаний закрылось.**
```sql
SELECT COUNT(*) AS total_companies_closed
FROM company
WHERE status = 'closed';
```

**2. Показать объём привлечённых средств для новостных компаний США, по убыванию.**
```sql
SELECT funding_total
FROM company
WHERE category_code = 'news' AND country_code = 'USA'
ORDER BY funding_total DESC;
```

**3. Показать имя, фамилию и название аккаунта людей, у которых аккаунт начинается на `Silver`.**
```sql
SELECT first_name, last_name, network_username
FROM people
WHERE network_username LIKE 'Silver%';
```

**4. Вывести всю информацию о людях, у которых в аккаунте есть `money`, а фамилия начинается на `K`.**
```sql
SELECT *
FROM people
WHERE network_username LIKE '%money%' 
AND last_name LIKE 'K%';
```

**5. Для каждой страны показать общую сумму привлечённых инвестиций, по убыванию.**
```sql
SELECT
    country_code,
    SUM(funding_total) AS total_funding
FROM company
GROUP BY country_code
ORDER BY total_funding DESC;
```

**6. Показать имя и фамилию всех сотрудников стартапов и учебное заведение, если оно известно.**
```sql
SELECT 
    p.first_name,
    p.last_name,
    e.instituition
FROM people p
LEFT JOIN education e ON e.person_id = p.id
ORDER BY p.id;
```

**7. Найти общую сумму сделок по покупке компаний за наличные с 2011 по 2013 год включительно.**
```sql
SELECT SUM(price_amount) AS total_cash_deals
FROM acquisition
WHERE term_code = 'cash'
  AND acquired_at BETWEEN '2011-01-01' AND '2013-12-31';
```

**8. Найти 10 самых активных стран-инвесторов среди фондов, основанных в 2010–2012 годах.**
Для каждой страны: минимальное, максимальное и среднее число компаний, в которые инвестировали фонды. Страны, где минимум равен нулю, исключить. Сортировка по среднему по убыванию, затем по коду страны.
```sql
SELECT
    country_code,
    MIN(invested_companies) AS min_companies,
    MAX(invested_companies) AS max_companies,
    AVG(invested_companies) AS avg_companies
FROM fund
WHERE founded_at BETWEEN '2010-01-01' AND '2012-12-31'
GROUP BY country_code
HAVING MIN(invested_companies) > 0
ORDER BY avg_companies DESC, country_code;
LIMIT 10;
```

---

## Контакты

- Email: <is.neznanov@yandex.ru>
- Telegram: <@neznanov_ilya>
