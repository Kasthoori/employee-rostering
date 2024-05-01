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
]



