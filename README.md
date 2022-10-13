# CI и CD для YaMDb
![example workflow](https://github.com/MysteryMister/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)
### Описание
Настройка CI и CD для проекта _api_yamdb_:

- автозапуск тестов,
- обновление образов на Docker Hub,
- автоматический деплой на боевой сервер при пуше в главную ветку _main_,
- отправка уведомления в Telegram о завершении процесса деплоя.
### Технологии
- Python 3.7
- Django 2.2.16
- gunicorn 20.0.4
- nginx
- docker 20.10.17
- GitHub Actions

### Запуск проекта (Windows)
1. Клонировать репозиторий и перейти в него:

    ```
    git clone git@github.com:MysteryMister/infra_sp2.git
    ```

    ```
    cd infra_sp2
    ```

2. Сделать коммит и запушить изменения:

    ```
    git add .
    ```

    ```
    git commit -m 'your comment'
    ```

    ```
    git push
    ```

3. Проверить состояние workflow в GitHub Actions.

#### Шаблон наполнения .env файла
DB_ENGINE=django.db.backends.postgresql

DB_NAME=postgres

POSTGRES_USER=test_user

POSTGRES_PASSWORD=test_password

DB_HOST=test_host

DB_PORT=1234

FROM_EMAIL=test@mail.ru

SECRET_KEY=test_key

### Адрес главной страницы
http://big-floppa.hopto.org/

http://158.160.2.129/

### Автор
Ли Георгий, 29 когорта, 2 тимворк
