# Learn Docker - DevOps with Node and Express

## Table of Contents

- [General Info](#general-information)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Configuration](#configuration)
- [Quick Start](#quick-start)
- [Project Status](#project-status)
- [Useful Commands](#useful-commands)
- [Acknowledgements](#acknowledgements)

## General Info

## Technologies

Project is created with:

- Docker
- Apache
- MariaDB
- Laravel 9

## Features

- coming soon

## Quick Start

```Javascript
// Docker is required

git clone the repo
cd laravel-docker

// build the docker containers
docker-compose up -d --build

// install laravel dependencies
docker exec php-apache composer install

//create the .env file
cp .env.example .env
docker-compose exec php-apache php artisan key:generate

//set permissions
docker exec php-apache chown -R www-data:www-data /var/www
docker exec php-apache chown -R 755 /var/www/laravel-docker/storage

// Project runs on http://localhost:8080
```

## Project Status

Project is in progress.

## Useful Commands

```Javascript

// Lists docker images
docker image ls

// Used to list containers
docker ps

// Run bash and browse docker files
docker exec -it containername bash

// List docker volumes
docker volume ls

// View contaner logs
docker logs containername -f

// Remove docker container with force flag
docker rm containername -f

// mongo shell
mongosh -u username -p password

docker system prune

```

## Acknowledgements

- This project is based on the [Learn Docker - DevOps with Node.js & Express](https://www.youtube.com/watch?v=9zUHg7xjIqQ) tutorial on YouTube.
