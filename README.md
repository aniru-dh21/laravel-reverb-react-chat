# Laravel Reverb: Real-Time Chat App

> In March of 2024, [Laravel 11 was released](https://blog.laravel.com/laravel-11-now-available). And with it arrived a new tool in the Laravel ecosystem: [Laravel Reverb](https://reverb.laravel.com/).

Reverb is a separate open-source package that's a first-party WebSocket server for Laravel applications. It helps facilitate real-time communication between client and server.

Before this new package, Laravel had event broadcasting, but basically it didn't have a built-in way to set up a self-hosted WebSocket server. Fortunately, Reverb now gives us that option.

Laravel Reverb has a few key features: it's written in PHP, i's fast, and it;s scalable. It was developed in particular to be horizontally scalable.

Reverb basically allows you to run an application on a single server - but if the application starts to outgrow that server, you can add multiple additional servers. Then those servers can all communicate with each other to distribute the messages between themselves.

## Installation

- **Prerequisites**
  - PHP >= 8.2
  - Composer
  - MySQL >= 5.7
  - Node.js >= 20

- Clone the repository, or download the zip file and extract it.
```shell
git clone git@github.com/aniru-dh21/laravel-reverb-react-chat.git && cd laravel-reverb-react-chat/
```

- Copy the `.env.example` file to `.env`:
```shell
cp .env.example .env
```

- Install the dependencies
```shell
composer install
```

- Generate the application key.
```shell
php artisan key:generate
```

- Create a MySQL database and set the database credentials in the `.env` file:
```shell
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE="<database_name>"
DB_USERNAME="<username>"
DB_PASSWORD="<password>"
```

- Setup Reverb credential in the `.env` file:
```shell
BROADCAST_CONNECTION=reverb

###

REVERB_APP_ID=
REVERB_APP_KEY=
REVERB_APP_SECRET=
REVERB_HOST="localhost"
REVERB_PORT=8080
REVERB_SCHEME=http

VITE_REVERB_APP_KEY="${REVERB_APP_KEY}"
VITE_REVERB_HOST="${REVERB_HOST}"
VITE_REVERB_PORT="${REVERB_PORT}"
VITE_REVERB_SCHEME="${REVERB_SCHEME}"
```

- Optimize the application cache.
```shell
php artisan optimize
```

- Run the migrations.
```shell
php artisan migrate:fresh
```
