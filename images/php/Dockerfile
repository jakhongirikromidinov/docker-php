FROM php:8.1-fpm


RUN apt-get update \
    && apt-get install -y curl git \
    && docker-php-ext-install mysqli pdo_mysql

WORKDIR /var/www/public_html

ENTRYPOINT [ "php-fpm" ]
