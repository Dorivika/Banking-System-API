# Django Banking System API

A RESTful Banking System API built with Django and Django Rest Framework (DRF).

## Features

- Bank and Branch management
- RESTful API endpoints
- Built with Django 3.2.9 and DRF 3.12.4
- Browsable API interface

## Prerequisites

- Python 3.x
- pip3
- virtualenv

## Quick Start

1. **Create and activate virtual environment:**
```bash
mkdir banksystem_project
cd banksystem_project
virtualenv .env
source .env/bin/activate
```

2. **Install dependencies:**
```bash
pip install django==3.2.9
pip install djangorestframework==3.12.4
pip install Markdown==3.3.6
pip install django-filter==21.1
```

3. **Set up Django project:**
```bash
django-admin startproject banksystem
cd banksystem
python manage.py startapp api
```

4. **Configure settings.py:**
```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'rest_framework',
    'api',
]
```

5. **Configure URLs (banksystem/urls.py):**
```python
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('api-auth/', include('rest_framework.urls')),
]
```

6. **Run migrations:**
```bash
python manage.py makemigrations
python manage.py migrate
```

7. **Start development server:**
```bash
python manage.py runserver
```

## Project Structure
```
banksystem_project/
├── banksystem/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── api/
│   ├── models.py
│   ├── views.py
│   ├── serializers.py
│   └── urls.py
└── manage.py
```

## API Endpoints

- `/api/banks/` - Bank operations
- `/api/branches/` - Branch operations
- `/api-auth/` - DRF authentication

## License

This project is licensed under the MIT License.
