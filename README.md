# django-commands
A repository that provides information about how to start a new project in Django.

# ATTENTION
This isn't the official Django's tutorial. It's just a simplified way to create a new project and start developing fast, avoiding waste of time with some mistaken commands. If you don't know anything about Django, it's highly recommended that you visit Django's official website [https://www.djangoproject.com/](https://www.djangoproject.com/).

## Index
- [Index](#index)
- [Description](#description)
- [Setup](#setup)
	- [venv](#venv)
		- [Activation](#activation)
		- [Deactivation](#deactivation)
	- [Installation](#installation)
- [Starting our project](#starting-our-project)
    - [django-admin](#django-admin)
- [Understanding our project](#understanding-our-project)
	- [manage.py](#manage.py)
- [Creating an app](#creating-an-app)
    - [app vs model](#app-vs-model)
    - [Example](#example)
- [Migrations](#migrations)
    - [makemigrations](#makemigrations)
    - [migrate](#migrate)
- [Let's see things working](#lets-see-things-working)
- [Congratulations and thanks](#congratulations-and-thanks)
- [Contribution](#contribution)
- [License](#license)
- [TODO](#todo)

## Description
When we work with frameworks, there are some basic rules that we may need to follow. The purpose of this repository is to help us keeping the right way when starting a new project in Django.

## Setup
First things first. Let's setup our work environment.

So, a good pratice, is to create our project inside a virtual environment. Why? Doing this, we protect all projects from each other. In other words, each Django project can have its own independent set of installed packages.

#### venv
Python's official library that provides this tool is [venv](https://docs.python.org/3/library/venv.html).
To create a virtual environmet, run:

```
python3 -m venv /path/to/new/virtual/environment
```

###### Activation
Now that we have created our virtual environment, let's active it:

```
source <venv>/bin/activate
```

Where *\<venv\>* is */path/to/new/virtual/environment*.

###### Deactivation
To deactive, just run:

```
deactivate
```

#### Installation
Alright, now that we have our work environment, let's install Django ~~finally~~. Remember: with virtual environment active, everything we install, will be installed inside our virtual environment. To **install** Django, run:

```
pip3 install django
```

## Starting our project
Django is a powerful framework to build web apps. It helps us building as many web apps as needed. But there is something on top of our web apps: our **BIG** project. The project is the web application itself and it holds lots of apps. To start our project, run:

```
django-admin startproject <project_name>
```

Don't forget to choose a good name :wink:

#### django-admin
From Django's official tutorial:
> **django-admin** is Django’s command-line utility for administrative tasks.

## Understanding our project
So far so good? Alright! At this point, our directory shall look like this:

```
project_name/
    manage.py
    project_name/
        __init__.py
        settings.py
        urls.py
        wsgi.py
```

#### manage.py
From Django's official tutorial:
> **manage.py**: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about **manage.py** in [django-admin and manage.py](https://docs.djangoproject.com/en/1.10/ref/django-admin/).

## Creating an app
Alright! Now it's time to put some **apps** inside our project. But first, let's understand the difference between an **app** and a **model**.

#### app vs model
From Django's official tutorial:
> A model is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Generally, each model maps to a single database table.

So, when we tell Django to start a an app, it creates a set of files and dependencies which will support all work on a model. The command to create a new app is:

```
python3 manage.py startapp <app_name>
```

#### Example
For example, we are writing a web application that manages an e-commerce. So, our project name is *MyCommerce* and we have this two apps, *Cart* and *Product*. Our project directory should look like this:

```
MyCommerce/:
    Cart/
        admin.py
        apps.py
        __init__.py
        migrations/
            __init__.py
        models.py
        tests.py
        views.py
    manage.py
    MyCommerce/
        __init__.py
        __pycache__/
            __init__.cpython-35.pyc
            settings.cpython-35.pyc
        settings.py
        urls.py
        wsgi.py
    Product/
        admin.py
        apps.py
        __init__.py
        migrations/
            __init__.py
        models.py
        tests.py
        views.py
```

## Migrations
Well done! We're almost ready to start developing our web application!

So, why Django is incredibly easy? One of the greatest things in Django is it's ability to handle lots of database's bureaucracy for us. It comes with an inner **SQLite** ready and working. All setted up.

Therefore, when we create an app and add some information to it's model, we are telling Django how is our database schema. 

#### makemigrations
To tell Django that our database schema (for a single model) is ready or updated, we run the following command:

```
python3 manage.py makemigrations <app_name>
```

#### migrate
And to tell Django "ok, now you can apply database changes", we run:

```
python3 manage.py migrate
```

## Let's see things working
Finally, to checkout our web application running:

```
python3 manage.py runserver
```

## Congratulations and thanks
Congratulations! Now everything is working, ready and waiting for your code. Thanks for arriving here. Hope you enjoyed this little tutorial.

## Contribution
I am still learning Django so, please, if you find any wrong information, submit an issue or create a pull request. Thanks! :octocat:

## License
[GPL-3.0](/LICENSE)

## TODO
- admin page
