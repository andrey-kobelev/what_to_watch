# Проект «Что посмотреть?»

> Сайт, который выдает случайные мнения о фильмах, поможет снять ответственность за выбор картины для просмотра и положиться на случай.

**Возможности для пользователей сайта:**

1. Получить случайное мнение о фильме.
2. Перейти на страницу конкретного мнения по прямой ссылке.
3. Добавить собственное мнение о фильме.

**Каждое мнение содержит:**
- название фильма,
- текст мнения,
- уникальную ссылку на страницу с мнением,
- ссылку на подробный обзор фильма на любом стороннем сервисе (эту информацию пользователь может не добавлять).


## Автор 
- Кобелев Андрей Андреевич  
    - [email](mailto:andrew.a.kobelev@yandex.ru)
  
## Технологии  
- [Python3.9](https://www.python.org/downloads/release/python-390/)
- [Flask](https://flask.palletsprojects.com/en/3.0.x/)
- [Flask-Migrate](https://flask-migrate.readthedocs.io/en/latest/)
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/3.1.x/)


## Как развернуть проект локально

**Клонировать репозиторий и перейти в него в командной строке:**

```
git clone https://github.com/andrey-kobelev/what_to_watch.git
```

```
cd what_to_watch
```

**Cоздать и активировать виртуальное окружение:**

```
python3 -m venv env  
```

```
source env/bin/activate  
```

**Установить зависимости из файла requirements.txt:**

```
python3 -m pip install --upgrade pip  
```

```
pip install -r requirements.txt  
```

**Создать файл .env**

```
FLASK_APP=opinions_app
FLASK_ENV=development
DATABASE_URI=sqlite:///the_app.sqlite3
```

**Создать базу данных**
Убедитесь, что виртуальное окружение проекта what_to_watch активировано, и из директории _what_to_watch_ запустите интерактивную оболочку:

```
..$ flask shell
Python 3.9.2 (v3.9.2:1a79785e3e, Feb 19 2021, 09:09:00) 
[Clang 12.0.0 (clang-1200.0.32.29)] on darwin
App: opinions_app [development]
Instance: /Users/username/dev/what_to_watch/instance
>>> from opinions_app import db
>>> db.create_all()
```

**Применить миграции:**

```
flask db upgrade
```

**Импортировать данные для демонстрации работы проекта**

```
flask load_opinions
```

**Запустить проект:**

```
flask run
```

