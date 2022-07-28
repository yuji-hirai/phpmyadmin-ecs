FROM php:8.1-fpm-bullseye

RUN apt-get update \
  && apt-get -y install --no-install-recommends default-mysql-client \
  && docker-php-ext-install pdo_mysql mysqli \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

COPY ./docker/php/php.ini /usr/local/etc/php/php.ini
COPY ./src /var/www/html
WORKDIR /var/www/html
RUN chown -R www-data:www-data ./