# django-commands
A repository that provides information about on how to develop web apps with django.

# ATTENTION
This isn't the official django tutorial. It's just a simplified way to create a new project and start developing fast, avoiding waste of time with some mistaken commands. If you don't know anything about django, it's highly recommended that you visit django's official website [https://www.djangoproject.com/](https://www.djangoproject.com/).

## Index
- [Index](#index)
- [Description](#description)
- [Setup](#setup)
	- [venv](#venv)
		- [Activation](#activation)
		- [Deactivation](#deactivation)
	- [Installation](#installation)
- [Starting our project](#starting-our-project)
    -[django-admin](#django-admin)
- [Understanding our project](#understanding-our-project)
	- [manage.py](#manage.py)
- [Creating an app](#creating-an-app)
- [Contribution](#contribution)
- [License](#license)

## Description
<p align="left">
When we work with frameworks, there are some basic rules that we may need to follow. The purpose of this repository is to help us keeping the right way when starting a new django project.
</p>

## Setup
<p align="left">
First things first. Let's setup our work environment.</p>
<p align="left">
So, a good pratice, is to create our project inside a virtual environment. Why? Doing this, we protect all projects from each other. In other words, each django project can have its own independent set of installed packages.
</p>

#### venv
Python's official library that provides this tool is [venv](https://docs.python.org/3/library/venv.html).
To create a virtual environmet, type:

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
To deactive, just type:

```
deactivate
```

#### Installation
Alright, now that we have our work environment, let's install django ~~finally~~. Remember: with virtual environment active, everything we install, will be installed inside our virtual environment. To **install** django, type:

```
pip install django
```

## Starting our project
Django is a powerful framework to build web apps. It helps us building as many web apps as needed. But there is something before our web apps: our **BIG** project. The project is the whole application and it can hold lots of little apps. To start our project, type:

```
django-admin startproject <project_name>
```

Don't forget to choose a good name :wink:

#### django-admin
From django's official tutorial:
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
From django's official tutorial:
> **manage.py**: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about **manage.py** in [django-admin and manage.py](https://docs.djangoproject.com/en/1.10/ref/django-admin/).

## Creating an app
<p align="left">
To be continued...
</p>

## Contribution
<p align="left">
I am still learning django so, please, if you find any wrong information, submit an issue or create a pull request. Thanks! :octocat:
</p>

## License
[GPL-3.0](/LICENSE)
