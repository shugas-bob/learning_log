# Learning Log

Веб-приложение на Django для ведения учебного журнала по темам и записям.

## Переменные окружения (`.env`)

Перед запуском на сервере заполните файл `.env`:

- `DJANGO_SECRET_KEY` — уникальный секретный ключ Django
- `DJANGO_DEBUG` — режим отладки (`False` для сервера)
- `DJANGO_ALLOWED_HOSTS` — разрешённые хосты (`192.168.1.11,localhost,127.0.0.1`)
- `DJANGO_CSRF_TRUSTED_ORIGINS` — доверенные источники (`http://192.168.1.11:<APP_PORT>`)
- `DJANGO_USE_HTTPS` — использование HTTPS (`False` при доступе по IP)
- `SQLITE_PATH` — путь к базе данных внутри контейнера (`/app/data/db.sqlite3`)
- `APP_BIND_IP` — IP привязки (`0.0.0.0`)
- `APP_PORT` — выделенный порт проекта

## Запуск �## Запуск �## З�

e```bash
docker compose up -d --build
```

Создание суперпользователя:

```bash
docker compose exec web python manage.py createsuperuser
```
