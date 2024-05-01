employee-rostering


Need to create .env file in root directory to add some configurations.
After that it need to load from .env file. In order to do that it need to
install decouple
pip3 install decouple

You can check installed dependencies using this command
pip3 freeze > requirement.txt 

=========================================================================

This is like microservices app. Therefore it needs to communicate with
front end. In order to do this, it requires to install corsheaders by 
using this command

pip3 install django-cors-headers

After installing this it needs to add following to setting.py file

INSTALLED_APPS = [
    ...,
    "corsheaders",
    ...,
]


MIDDLEWARE = [
    ...,
    "corsheaders.middleware.CorsMiddleware",
    "django.middleware.common.CommonMiddleware",
    ...,
]

CORS_ALLOWED_ORIGINS = [
    "https://example.com",
    "https://sub.example.com",
    "http://localhost:8080",
    "http://127.0.0.1:9000",

    "http://localhost:3000" -> this need to add if connect with React Frontend. 
]

If work with django rest framework it need to install rest framework

pip3 install djangorestframework
pip3 install markdown       # Markdown support for the browsable API.
pip3 install django-filter  # Filtering support

INSTALLED_APPS = [
    ...
    'rest_framework',
]

urlpatterns = [
    ...
    path('api-auth/', include('rest_framework.urls'))
]

it need to install python-decouple

pip3 install python-decouple

Now need to issue following command

python3 manage.py makemigrations

and 

python3 manage.py migrate

This create and update database

You can run the server by

python3 manage.py runserver

Next thing to work registration router it need to install allauth

pip3 install allauth

Then need to include "allauth.account" to setting.py



