# Проект «API для Yatube»
## Кратко о проекте
Данный проект - реализация API для другого учебного проекта Yatube.
API необходим для унифицированного доступа к функциям проекта Yatube.
С помощью API можно работать с проектом Yatube при помощи запросов, а не использовать для этого ручные операции.
Наличие API повышает безопасность, универсальность, мобильность и доступность проекта Yatube.

## ENV-файл
Файл имеет структуру:

`DB_ENGINE=#######` - указываем, что работаем с postgresql

`DB_NAME=#######` - имя базы данных

`POSTGRES_USER=#######` - логин для подключения к базе данных

`POSTGRES_PASSWORD=#######` - пароль для подключения к БД

`DB_HOST=#######` - название сервиса (контейнера)

`DB_PORT=#######` - порт для подключения к БД 

где '######' это ваши данные

## Запуск приложения в контейнерах
Для запуска контейнеров: `docker-compose up -d`

Далее выполните по очереди команды:

```
docker-compose exec web python manage.py migrate

docker-compose exec web python manage.py createsuperuser

docker-compose exec web python manage.py collectstatic --no-input
```


## Заполнения базы данными
Для загрузки данных в БД используйте команду:

`docker-coppose exec web python manage.py loaddata fixtures.json`

## Автор
Сергей,

Студент факультета Backend-разработки в Яндекс.Практикум.

## Используемые технологии

* Django
* Docker
* NGINX