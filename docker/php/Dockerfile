FROM php:8.1.0-fpm-alpine
RUN apk add --no-cache curl git zlib-dev bash build-base oniguruma-dev autoconf
RUN pecl install xdebug && docker-php-ext-enable xdebug
COPY xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini
WORKDIR /app
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer