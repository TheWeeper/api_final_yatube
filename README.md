# api_final
## Описание
Yatube API — это RESTful API, предназначенной для публикации постов, комментирования и подписки на авторов. Проект предоставляет удобный интерфейс для взаимодействия с контентом платформы через API-запросы.  
Проект позволяет пользователю создавать, редактировать и удалять посты, комментироать публикации других пользователей, подписываться и отслеживать других авторов.
## Установка
Для того чтобы запустить проект необходимо клонировать репозиторий и перейти в него с помощью командной строки:
```

cd yatube_api/
```
Создать и активировать виртуальное окружение:
```
py -3.9 -m venv venv
source venv/Scripts/activate
```
Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```
Выполнить миграции:
```
python manage.py migrate
```
Запустить проект:
```
python manage.py runserver
```
## Примеры
Получить список всех постов:
```
GET http://127.0.0.1:8000/api/v1/posts/
```
Добавление новой публикации в коллекцию публикаций:
```
POST http://127.0.0.1:8000/api/v1/posts/
```
Удаление публикации по id:
```
DELETE http://127.0.0.1:8000/api/v1/posts/{id}/
```
Подписка пользователя от имени которого сделан запрос на пользователя переданного в теле запроса:
```
POST http://127.0.0.1:8000/api/v1/follow/
```
