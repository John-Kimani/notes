# Introduction


# Lets get started
1. Create a folder to host your django application.
2. I recommend setting up a virtual environment for each and every application you build using the django framework.

## Install django framework
Open terminal in your project directory:
Run
```bash
    virtualenv virtual
```
or
```bash
    python3 -m venv virtual
```

This command will create a python virtual environment named "virtual" in your project directory.

Activate your virtual environment:
Run
```bash 
source virtual/bin/activate
```
Then,
Install Django
Run
```bash
(virtual) pip install django
```
or you can use python buit in pip module
Run
```bash
(virtual) python -m pip install django
```
Any of the above commands should install the latest current version of django.

However, it is important to check the django version installed in your virtual environment.

On your terminal, open the python shell
Run
```bash
(virtual) python
```
or
```bash
(virtual) python3
```
This command will issue a prompt in python shell run codes below to check django version installed.
```bash
(virtual)
    >>> import django
    >>> django.get_version()

output:
>>> '4.0.3'
```
I used django version (4.0.3) as it was the current LTS when writing this documentation.

#### Set up Requirements
Run:
```bash
(virtual) touch requirements.txt
```
Create a requirements file in your project root folder.

To get us started, I would recommend having:
```
asgiref==3.5.0
backports.zoneinfo==0.2.1
Django==4.0.3
gunicorn==20.1.0
python-decouple==3.6
sqlparse==0.4.2
```

Other than django, I have python-decouple and gunicorn and pycopg2

This pips are relevant to handle various app functionalities. Refer more about pip and other python related environment setups from  [pyp.org](https://pypi.org/)

Install python-decouple run:
```bash
    pip install python-decouple
```
Python decouple pip enables us to access hidden files such as .env files where we store our secret configurations.

Install psycopg2 run:
```bash
    pip install psycopg2
```
For this project I will be using a PostgreSQL database, [psycopg2](https://pypi.org/project/psycopg2/) is a PostgreSQL database adapter.

Install gunicorn, run:
```bash
    pip install gunicorn
```
This comes in handy when deploying django project on heroku learn more [gunicorn](https://pypi.org/project/gunicorn/)

## Start django project
On your terminal, ensure that your virtual env is activated:

Run:
```bash
django-admin startproject <name_of_your_project>
```
or
```bash
django-admin startproject <name_of_your_project> .
```
These commands with create a new folder in your current directory.

That's not all, note the period sign at the end of the second command, the (.) sign is used for a so called "better folder structure" such that your special django file "manage.py" will be on your project root folder unlike having in on a separate folder like in the first command.

Run:
```bash
(virtual) python manage.py runserver
```

to test your project on a development server. On your local server address you will be greeted with the default django project welcome page.