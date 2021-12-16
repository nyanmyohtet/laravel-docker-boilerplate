# Laravel Docker Boilerplate

## Technologies

- PHP: 7.3
- Laravel: 8.x
- Composer: 2.x

## GitHub App

- [RenovateBot](https://app.renovatebot.com)

## Setup

Build docker container(optional)

`docker-compose build`

Start docker containers

`docker-compose up -d`

Install Laravel Framework

`docker-compose exec app rm .gitignore`

`docker-compose exec app composer create-project --prefer-dist laravel/laravel . "8.*"`

Change `laravel/.env`

```
DB_CONNECTION=mysql
DB_HOST=database
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=password
```

Migrate Database

`docker-compose exec app php artisan migrate`

App is running at http://localhost:8000.

PHPMyAdmin is running at http://localhost:8080.

SSH into 'app' container

`docker-compose exec app ash`
