# Laravel Docker Boilerplate

## Technologies

- Laravel: 6.x
- Composer: 2.x

## Setup

Start docker containers

`docker-compose up -d`

Install Laravel Dependencies

`docker run --rm -v "$(pwd)/laravel:/app" composer install --no-scripts`

Copy ".env" file

`docker-compose exec app cp .env.example .env`

Generate APP_KEY

`docker-compose exec app php artisan key:generate`

Migrate Database

`docker-compose exec app php artisan migrate`

App is running at http://localhost:8080.

SSH into 'app' container

`docker-compose exec app ash`
