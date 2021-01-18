FROM php:7.4-apache
RUN apt-get update && docker-php-ext-install mysqli pdo pdo_mysql
RUN rm /etc/apt/preferences.d/no-debian-php
RUN apt-get update -y && apt-get install -y libwebp-dev libjpeg62-turbo-dev libpng-dev libxpm-dev \
  libfreetype6-dev
RUN apt-get update && \
  apt-get install -y \
  zlib1g-dev

RUN apt-get install -y libzip-dev
RUN docker-php-ext-install zip gd
RUN apt-get install -y zip unzip php-zip

# RUN docker-php-ext-configure gd --with-gd --with-webp-dir --with-jpeg-dir \
#   --with-png-dir --with-zlib-dir --with-xpm-dir --with-freetype-dir \
#   --enable-gd-native-ttf
# RUN docker-php-ext-install gd
RUN a2enmod rewrite

WORKDIR /var/www/html
