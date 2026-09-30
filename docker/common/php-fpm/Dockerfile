FROM php:8.4-fpm AS base

WORKDIR /var/www

# Required libs and PHP extensions + cleanup

RUN apt-get update && apt-get install -y --no-install-recommends \
    libbz2-dev \
    zlib1g-dev \
    libpng-dev \
    libicu-dev \
    libxml2-dev \
    libxslt1-dev \
    libzip-dev \
    libavif-dev \
    libwebp-dev \
    libjpeg-dev \
    libxpm-dev \
    libfreetype-dev \
    && docker-php-ext-configure gd --with-jpeg --with-avif --with-freetype --with-xpm --with-webp \
    && docker-php-ext-install \
    bcmath \
    bz2 \
    calendar \
    exif \
    ftp \
    gd \
    gettext \
    intl \
    mysqli \
    pcntl \
    pdo_mysql \
    shmop \
    soap \
    sockets \
    xsl \
    zip \
    && apt-get autoremove -y && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Composer image

COPY --from=composer:2 /usr/bin/composer /usr/bin/