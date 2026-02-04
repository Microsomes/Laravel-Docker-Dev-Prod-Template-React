FROM php:8.2-fpm
WORKDIR /var/www

################################################################################
##
##      Install dependencies
##
RUN apt-get update \
    && apt-get install -y sqlite3 mariadb-client libjpeg-dev libpng-dev libonig-dev libzip-dev unzip \
        && docker-php-ext-install     bcmath pdo_mysql pcntl \
        && docker-php-ext-configure   gd --with-jpeg  \
        && docker-php-ext-install     gd  \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

USER    33
EXPOSE  9000
CMD     ["php-fpm"]
