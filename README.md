# social_media_site

## Django setup
    python3 -m venv env
    source env/bin/activate
    pip3 install django
    pip3 install django-crispy-forms 
    pip3 install crispy-bootstrap4

## Application
    django-admin startproject <project_name> (example project_name: social_media_site)
    cd <project_name>/   (example project_name: social_media_site)
    python manage.py runserver
    python manage.py startapp <app_name> (example app_name: post)
    python manage.py makemigrations  <app_name> (Run when a new data model is added to the app. Example app_name: todo)
    python manage.py migrate  (Run to create the table for a new data model. Example app_name: todo)

## Debugging
    python manage.py shell (To create a shell where one can interact with the sql db.)

## Super user for admin:
    python manage.py createsuperuser