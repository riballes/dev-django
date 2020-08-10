# First App in Django

## Creating a Project

First thing first, we need to auto-generate some code that establishes a Django [project](#Glossary).

Let's get started. From the command line, cd into a directory where you would like to store your code and run the following command:

```
$ cd <desired_directory>
$ django-admin startproject <project_folder_name>
```

If we use as project folder name **_mysite_** We have the following structure comming from [startproject](https://docs.djangoproject.com/en/3.1/ref/django-admin/#django-admin-startproject):

```
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```
For more details on the structure, click [Startproject file structure](#Startproject-file-structure).

## Creating Polls

Now that our environment – a “project” – is set up, we can start doing work.

Each application you write in Django consists of a Python package that follows a certain convention. Django comes with a utility that automatically generates the basic directory structure of an app, so you can focus on writing code rather than creating directories.

Your apps can live anywhere on your Python path. For this example, we’ll create our poll app in the same directory as our manage.py file so that it can be imported as its own top-level module, rather than a submodule of _mysite_.

To create your app, make sure you’re in the same directory as manage.py and type this command:

```
$ python manage.py startapp polls
```

That’ll create a directory polls, which is laid out like this:

```
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```


## Startproject file structure

* The outer **mysite/** root directory is a container for your project. Its name doesn’t matter to Django; you can rename it to anything you like.
* **manage.py:** A command-line utility that lets you interact with this Django project in various ways.
* The inner **mysite/** directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. mysite.urls).
* **mysite/__init__.py:** An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read more about packages in the official Python docs.
* **mysite/settings.py:** Settings/configuration for this Django project. Django settings will tell you all about how settings work.
* **mysite/urls.py:** The URL declarations for this Django project; a “table of contents” of your Django-powered site.
* **mysite/asgi.py:** An entry-point for ASGI**-compatible web servers to serve your project.
* **mysite/wsgi.py:** An entry-point for WSGI-compatible web servers to serve your project.

##  Glossary

* **Project:** A Python package – i.e. a directory of code – that contains all the settings for an instance of Django. This would include database configuration, Django-specific options and application-specific settings.

