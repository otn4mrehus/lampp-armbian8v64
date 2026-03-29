FROM php:7.4-apache

# Install dependencies
RUN apt-get update -y && apt-get install -y \
    libpng-dev \
    libjpeg62-turbo-dev \
    libfreetype6-dev \
    libonig-dev \
    libzip-dev \
    zip \
    unzip \
    && docker-php-ext-configure gd \
        --with-freetype \
        --with-jpeg \
    && docker-php-ext-install gd mbstring zip mysqli pdo_mysql

# Enable Apache mod_rewrite
RUN a2enmod rewrite

# Set Document Root
WORKDIR /var/www/html
