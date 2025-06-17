# Лабораторная работа по Backend (Express): подготовка веб-сайта

В рамках лабораторной работы было выполнено создание основы для сервера библиотеки. В будущем ее можно доработать до веб-сайта, где пользователи смогут просматривать книги.

## Задание

В ходе работы были выполнены первые 3 этапа из туториала [официального руководства MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Tutorial_local_library_website):

1. Настройка среды разработки Node
2. Создание каркаса веб-сайта
3. Подключение и работа с MongoDB (включая тестирование скриптом `populatedb.js`)

## Результаты

- Сервер успешно запускается и обрабатывает запросы
- Скрипт `populatedb.js` корректно заполняет базу данных тестовыми данными
- Подключение к MongoDB Atlas настроено и работает стабильно

Пример данных в таблице `authors` в [MongoDB Atlas](https://www.mongodb.com/products/platform/atlas-database)
![Просмотр данных авторов в MongoDB Atlas](https://github.com/user-attachments/assets/67caf3e7-d80e-4785-94ad-8505f2e46b5d)

## Быстрый старт

Чтобы запустить этот проект локально на вашем компьютере:

1) Настройте среду разработки [Node.js](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/Express_Nodejs/development_environment).

2) После настройки Node клонируйте этот репозиторий и установите зависимости:
```
install npm
```
3) Настройте подключение к БД. Создайте `.env` файл в корне проекта и заполните его по образцу:
```
DB_USER=your_username
DB_PASS=your_password
DB_HOST=your_cluster_host
DB_NAME=your_database_name
```

3) Для запуска в режиме разработки используйте соответствующую для вашей среды команду:
```
# Терминал Linux
 DEBUG=express-locallibrary-tutorial:* npm run devstart

# Windows Powershell
$ENV:DEBUG = "express-locallibrary-tutorial:*"; npm start
```

4) Заполните базу данных тестовыми значениями
```
node populatedb <your MongoDB url>
```

5) Откройте http://localhost:3000/ - ссылку будущего сайта библиотеки.
