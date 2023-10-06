# Blog-App
Blog Application
# HireCoderApi

Based on Django `4.2.4`

## Getting Started

Setup project environment with [virtualenv](https://virtualenv.pypa.io) and [pip](https://pip.pypa.io).

```bash
$ virtualenv project-env
$ source project-env/bin/activate
$ pip install -r requirements/dev.txt

# get the latest .env from your fellow developer, or copy same from infra/dotenvsample.
$ touch backend_restructure/.env

$ cd backend_restructure/
$ python manage.py migrate
$ python manage.py runserver
```


## First Time Use

* Create a superuser using [this guide](https://www.geeksforgeeks.org/how-to-create-superuser-in-django/).

## Database or other errors
At this point in time this application works with any database backend, so please replace this in the `app/srp/settings.py` 
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': config('DB_NAME'),
        'USER': config('DB_USER'),
        'PASSWORD': config('DB_PASSWORD'),
        'HOST': config('DB_HOST'),
        'PORT': config('DB_PORT'),
    }
}
```
with 
```python
DATABASES['default'] = {'ENGINE','django.db.backends.sqlite3', 'NAME': 'srp_test', }
```

## Contributing

I love contributions, so please feel free to fix bugs, improve things, provide documentation.
