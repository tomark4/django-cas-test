
### instalacion

`virtualenv -p python3 venv`

`. venv/bin/activate`

Esta app (auth) sera el servido de autenticacion cas

`cd auth && pip install -r requirements.txt && python manage.py migrate &&
`
`python manage.py createsuperuser`

`python manage.py runserver`

Esta app (shop) sera el cliente de autenticacion

    - La corremos en otro puerto para poder conectarnos al server cas en la app
(auth)

`cd shop && pip install -r requirements.txt && python manage.py runserver
localhost:4000`


