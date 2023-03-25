# Cinema API

API service for cinema management written on DRF

## Installing using GitHub

Install PostgreSQL and create database.

1. Clone project and create virtual environment

```shell
git clone https://github.com/yuliia-stopkyna/cinema-api.git
cd cinema-api
python -m venv venv
source venv/bin/activate # on MacOS
venv\Scripts\activate # on Windows
pip install -r requirements.txt
```
2. Set environment variables

On Windows use ```export``` command instead of ```set```
```shell
set POSTGRES_HOST=<your db host>
set POSTGRES_DB=<your db name>
set POSTGRES_USER=<your db user>
set POSTGRES_PASSWORD=<your db password>
set SECRET_KEY=<your Django secret key>
```
3. Make migrations and run server

```shell
python manage.py migrate
python manage.py runserver
```
## Run with docker

Docker should be installed.

Create ```.env``` file with your environment 
variables (look at ```.env.sample``` example file).


```shell
docker-compose build
docker-compose up
```
## Features

* JWT authenticated
* Admin panel /admin/
* Documentation at /api/doc/swagger/
* Managing orders and tickets
* Creating movies with genres, actors
* Creating cinema halls
* Adding movie sessions
* Filtering movies and movie sessions

## Getting access

* create user via /api/user/register/
* get access token via /api/user/token/
