FROM php:8.2-fpm

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

ENV PACKAGES="git curl zip unzip libfreetype-dev libjpeg62-turbo-dev libpng-dev libzip-dev libicu-dev libxml2-dev"

RUN apt-get update && apt-get install -y ${PACKAGES}
#	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
#	&& docker-php-ext-install -j$(nproc) gd

#RUN docker-php-ext-install -j$(nproc) mysqli pdo_mysql zip sockets exif intl gettext soap opcache pcntl xml
