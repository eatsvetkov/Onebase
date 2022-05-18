## Первые шаги

### Установить django

`pip install Django`

### Создать проект

`django-admin startproject nameproject`

### Запустить локальный сервер

Переходим в папку onecontrol

`cd C:\Users\Server\Desktop\onecontrol`

Переходим в папку smatrplug

`cd C:\Users\Server\Desktop\smartplug\Server\WebVersion\unisy.ru\FetchData`

`python manage.py runserver`

`Ctrl+C` закрыть runserver

### Создать новое приложение

`python manage.py startapp mainpage`

### Изменение bootstrap

[Видеоурок по настройке node и npm](https://www.youtube.com/watch?v=-eo_1tsTKks)

Все кастомы хранятся в файле scss\customization.scss

В файле bootstrap.scss первым вызывается файл кастомов и переопределяет настройки.

Данный метод очень удобен для обновления bootstrap

#### Переходим в папку bootstrap

`cd C:\Users\Server\Desktop\onecontrol\mainapp\static\bootstrap-5.1.0`

#### Запускаем генерирование файлов

`npm run dist`

### Миграция моделей

`python manage.py makemigrations`

`python manage.py migrate`

## Перенос сайта на хостинг

### Установка Dajngo

В первую очередь необходимо установить Django на хостинге по инструкции поставщика услуг. 

Пример reg.ru:

[Как установить Django на хостинг](https://help.reg.ru/hc/ru/articles/4408047456785-%D0%9A%D0%B0%D0%BA-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-Django-%D0%BD%D0%B0-%D1%85%D0%BE%D1%81%D1%82%D0%B8%D0%BD%D0%B3)

### Перенос с локального компьютера

[Развертывание Django-сайта на хостинге](https://www.youtube.com/watch?v=6W9P4AnlwHI&list=PLA0M1Bcd0w8xO_39zZll2u1lz_Q-Mwn1F&index=26)

## Полезные ссылки

[Форма с использованием модели без Createview](https://www.youtube.com/watch?v=VOddmV4Xl1g)

