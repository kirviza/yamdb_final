# Инструкция проекта infra_sp2
infra_sp2

## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/kirviza/infra_sp2.git
cd infra_sp2/infra/
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
