
### instalacion

`git clone https://github.com/tomark4/django-cas-test.git`

`cd django-cas-test`

`virtualenv -p python3 venv`

`. venv/bin/activate`

Esta app (auth) sera el servicio de autenticación cas

`cd auth && cp .env.example .env && pip install -r requirements.txt`

`python manage.py shell`

#### generar la SECRET_KEY del proyecto
$ from django.core.management.utils import get_random_secret_key
$ get_random_secret_key()

copiar la key en el archivo .env

`python manage.py migrate`

`python manage.py createsuperuser`

`python manage.py runserver`

Esta app (shop) sera el cliente de autenticación

    -La corremos en otro puerto para poder conectarnos al server cas en la app
(auth)

`cd shop && pip install -r requirements.txt && python manage.py runserver localhost:4000`


