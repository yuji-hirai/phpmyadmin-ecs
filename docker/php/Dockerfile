FROM php:8.1-fpm-bullseye

WORKDIR /var/www/html

RUN apt update \
  && apt install -y default-mysql-client \
  && docker-php-ext-install pdo_mysql mysqli

COPY ./src /var/www/html
RUN chown -R www-data:www-data /var/www/html
COPY ./docker/php/php.ini /usr/local/etc/php/php.ini