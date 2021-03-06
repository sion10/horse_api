# horse_api

## Overview

## Description

## Demo

## Requirement

- Nginx
- Anaconda
- PostgreSQL(=>9.3)
- pyenv-pip-rehash
- build-essential
- python3-dev
- libpq-dev
- uwsgi(pip package)
- psycopg2(pip package)
- Flask-SQLAlchemy(pip package)
- Flask-Migrate(pip package)
- beautifulsoup4(pip package)

If you use Chef, you can clone cookbooks from below to provision an environment.
This cookboos include pip package.

[flask-env](https://github.com/ttaka66/flask-env)

You can also install just pip package from below command.

```bash:
$ pip install -r requirements.txt
```

## Usage

### Config

You must make config.py file under horse_api/application directory.

```bash:
$ vim horse_api/application/config.py
```

config.py
```python:config.py:
SQLALCHEMY_DATABASE_URI = 'postgresql://YOUR_DB_SERVER/YOUR_DB'
SECRET_KEY = 'YOUR_SECRET_KEY'
SQLALCHEMY_TRACK_MODIFICATIONS = True
ADMINNAME = 'YOUR_ADMINISTRATOR_NAME'
PASSWORD = 'YOUR_ADMINISTRATOR_PASSWORD'
```

### Create table

You can create all tables from below command.

```bash:
$ python manage.py init_db
```

### Drop table

You can drop all tables from below command.

```bash:
$ python manage.py drop_db
```

## Run

#### uWSGI

Paste the following command at a Terminal prompt.

```bash:
$ cd horse_api/
$ uwsgi --ini myapp.ini
```

#### Debug

Paste the following command at a Terminal prompt.

```bash:
$ cd horse_api/
$ python manage.py runserver --host 0.0.0.0 --debug --reload
```

## Contribution

## Licence

## Author
