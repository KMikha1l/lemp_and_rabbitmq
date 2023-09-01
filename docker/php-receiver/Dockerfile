FROM composer:2.5.4 as composer
FROM phpdockerio/php:8.2-fpm
WORKDIR "/application"

RUN apt-get update; \
    apt-get -y --no-install-recommends install \
        git \
        php-xdebug \
        php8.2-mysql \
        php8.2-sqlite \
        mysql-client \
        php8.2-redis; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

WORKDIR /application/src/public
CMD [ "php", "./rabbit_consumer.php" ]


#RUN pecl install xdebug \
#&& docker-php-ext-enable xdebug
