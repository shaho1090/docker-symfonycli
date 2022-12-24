FROM php:8.1-fpm

RUN apt update \
    && apt install -y zlib1g-dev g++ git libicu-dev zip libzip-dev zip \
    && docker-php-ext-install intl opcache pdo pdo_mysql \
    && pecl install apcu \
    && docker-php-ext-enable apcu \
    && docker-php-ext-configure zip \
    && docker-php-ext-install zip

ENV COMPOSER_ALLOW_SUPERUSER = 1

COPY --from=composer:2.4 /usr/bin/composer /usr/bin/composer

COPY ./app/composer.* ./

#RUN composer install --prefer-dist --no-dev --no-scripts --no-progress --no-interaction

COPY ./app .

RUN curl -sS https://get.symfony.com/cli/installer | bash

#RUN mv /root/.symfony5/bin/symfony /usr/local/bin/symfony

#RUN composer dump-autoload --optimize