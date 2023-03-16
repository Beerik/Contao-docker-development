# Docker dev-env update

### Alpine3.17 + nginx, php8.1, php7.4, Mysql5.7

## Requirements

- docker 1.10.0+
- compose V2+ (https://docs.docker.com/compose/install/)

## Basic Setup

- clone or download and unpack repository
- cd to project folder
- run the following to build and run the containers
  > $ docker compose build \
  > $ docker compose up ("-d" for detached mode)

## PHP config

- open /build/nginx/config/server.conf
- add new <code>server{}</code> block including the required configuration file
  - <code>include fpm-no-contao.conf</code> - basic php config using php8.1-fpm
  - <code>include fpm-php74.conf</code> - basic php config using php7.4-fpm container
  - <code>include fpm-contao4.conf</code> - contao 4.x config using php8.1-fpm
