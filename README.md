![example workflow](https://github.com/kirviza/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

ip адресс сервера: http://51.250.110.238/admin/

# Инструкция проекта yamdb_final
yamdb_final

## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/kirviza/yamdb_final
cd yamdb_final/infra/
```

Выполнить команду по сборке контейнера:
```
docker-compose up -d --build 
```

Выполнить миграции:
```
docker-compose exec web python manage.py migrate
```

Создать суперпользователя:
```
docker-compose exec web python manage.py createsuperuser
```

Собрать статичные файлы:
```
docker-compose exec web python manage.py collectstatic --no-input
```

Описание проекта:
```
Проект представляет из себя социальную сеть в которой можно оставлять отзывы на 
фильмы или книги и ставить оценки.
А так же комментировать отзывы.
```

## Настройка workflow
Добавьте в Secrets GitHub Actions следующие переменные окружения:
```
DB_ENGINE
DB_HOST
DB_NAME
DB_PORT
DOCKER_PASSWORD
DOCKER_USERNAME
HOST ip адрес сервера
POSTGRES_PASSWORD
POSTGRES_USER
SSH_KEY приватный ключ с локального компьютера
TELEGRAM_TO токен аккаунта на который присылать сообщение
TELEGRAM_TOKEN токен бота
USER логин сервера на облаке
```

Автор:
```
Мыши Рокеры
```

Технологии которые использовались:
```
-Python
-Django
-rest_framework
-djoser
-postgreSQL
-nginx
-docker
```
