# README #

This README would normally document whatever steps are necessary to get your application up and running.

### What is this repository for? ###

Bondstreet Interview Questions

### How do I get set up? ###

All the necessary modules used are in requirements.txt.

You should install everything in requirements.txt to get up and running.

The main stack consists of:

Python 2.7

Django

Postgresql - Postgres Database Server and Client

Psychodb2 - Postgres Python Library

Bootstrap 3.x for CSS and Frontend UI

webapp - is the main Django project under which many apps can live

statekeeper - An App that keeps the state of the Application and User while using the system

### Required tasks - Load data at runtime ###

#### This loads up the application states that the workflow app relies on
python manage.py loaddata statekeeper/fixtures/load_states.json 

### Design Considerations ###

Why are you using postgres: My system is setup to use Postgres and I am comfortable with it. I also wanted to persist data in a relational database and not another type of data store

Why are you using django: I made decision to use Django as opposed to Flask because:
1. Need to an ORM
2. Ease of User management, Sessions, Authentication
3. Easy migrations
4. Built in tools for building models.
5. Knowledge and comfort with the tool.


### results from the project ###

The user needs to be validated and can start the loan application process.
Sessions are maintained. The user can leave a page and return to the last application workflow.
The Application workflow is remembered for the user and the user upon login is taken to the last place completed.
The user can go back using the dropdown but cannot skip ahead.
The application records state at each process. Upon completion the user is logged out.