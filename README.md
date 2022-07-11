# Docker-compose для YaMDb
### Описание
Запуск проекта _api_yamdb_ в контейнере через _docker-compose_.
### Технологии
- Python 3.7
- Django 2.2.16
- gunicorn 20.0.4
- nginx
- docker 20.10.17

### Запуск проекта (Windows)
1. Клонировать репозиторий и перейти в его поддиректорию _infra_:

    ```
    git clone git@github.com:MysteryMister/infra_sp2.git
    ```

    ```
    cd infra_sp2/infra
    ```

2. Запустить проект в контейнере:

    ```
    docker-compose up -t --build
    ```

3. Выполнить миграции:

    ```
    docker-compose exec web python manage.py migrate
    ```

4. Загрузить фикстуры в БД:

    ```
    docker-compose exec web python manage.py loaddata fixtures.json
    ```

#### Шаблон наполнения .env файла
DB_ENGINE=django.db.backends.postgresql

DB_NAME=postgres

POSTGRES_USER=test_user

POSTGRES_PASSWORD=test_password

DB_HOST=test_host

DB_PORT=1234

FROM_EMAIL=test@mail.ru

SECRET_KEY=test_key

### Автор
Ли Георгий, 29 когорта, 2 тимворк
