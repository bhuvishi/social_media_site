# social_media_site

## Create base dir and env.
    mkdir social_media_site && cd social_media_site
    python3 -m venv env
    source env/bin/activate

## Clone project to your machine.
    git clone https://github.com/bhuvishi/social_media_site.git
    cd social_media_site

## Install required packages
    pip install -r requirements.txt

## Migrate project
    python3 manage.py makemigrations
    python3 manage.py migrate

## Run your server on your localhost
    python3 manage.py runserver

## Deployment
    https://www.codingforentrepreneurs.com/blog/rds-database-serverless-django-zappa-aws-lambda/
    python manage.py collectstatic
    zappa manage dev "collectstatic --noinput"
    zappa update dev
    zappa manage dev create_pg_db
    zappa update dev
    zappa manage dev migrate

## Super user for admin:
    zappa manage dev create_admin_user
    zappa update dev

## Debugging
    python manage.py shell (To create a shell where one can interact with the db.)