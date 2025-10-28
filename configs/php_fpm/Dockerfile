# Use the official PHP-FPM image
FROM php:8.2-fpm

# Copy PHP configuration file
COPY php.ini /usr/local/etc/php/conf.d/php.ini

# Install necessary packages and PHP extensions
RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libwebp-dev \
    libxpm-dev \
    git \
    unzip \
    wget \
    curl \
    && docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp \
    && docker-php-ext-install gd pdo pdo_mysql bcmath ctype fileinfo json mbstring openssl tokenizer xml \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Install Composer globally
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Verify installation
RUN php -v && composer --version
