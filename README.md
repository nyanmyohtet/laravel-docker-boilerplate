# Laravel Docker Boilerplate

## Technologies

- Laravel: 6.x
- Composer: 2.x

## GitHub App

- [RenovateBot](https://app.renovatebot.com)

## Setup

Build docker container(optional)

`docker-compose build`

Start docker containers

`docker-compose up -d`

Install Laravel Framework

`docker-compose exec app composer create-project --prefer-dist laravel/laravel . "6.*"`

Install Laravel Dependencies(Run with PowerShell)

`docker run --rm -v "$(pwd)/laravel:/app" composer install --no-scripts`

Copy ".env" file

`docker-compose exec app cp .env.example .env`

Generate APP_KEY

`docker-compose exec app php artisan key:generate`

Migrate Database

`docker-compose exec app php artisan migrate`

App is running at http://localhost:8000.

PHPMyAdmin is running at http://localhost:8080.

SSH into 'app' container

`docker-compose exec app ash`
