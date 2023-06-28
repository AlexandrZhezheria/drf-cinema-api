# DRF Cinema API

API service for cinema management written on Django REST Framework

## Installing using GitHub:
Install PostgresSQL and create db.
```
git clone https://github.com/AlexandrZhezheria/drf-cinema-api.git
cd drf_cinema_api
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
mv .env.sample .env
```
Place expected values of all variables into .env.sample for Linux or into env.bat.sample for Windows:
```
POSTGRES_HOST={POSTGRES_HOST}
POSTGRES_NAME={POSTGRES_NAME}
POSTGRES_USER={POSTGRES_USER}
POSTGRES_PASSWORD={POSTGRES_PASSWORD}
SECRET_KEY={SECRET_KEY}
```
On Linux run:
```
mv .env_sample .env
source .env
sh start.sh
```
On Windows run:
```
ren .env_sample .env
env.bat
bash start.sh
```


## Run with Docker:
```
docker-compose build
docker-compose up
```

## Getting access:
- create user via /api/user/register/
- get a JWT token via /api/user/token/

## Features:
- JWT authenticated
- Admin panel /admin/
- SWAGGER documentation /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions
