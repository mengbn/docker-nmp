FROM php:7.1-fpm-alpine

# Packages
RUN apk --update add \
    autoconf \
    build-base \
    linux-headers \
    libaio-dev \
    zlib-dev \
    curl \
    git \
    subversion \
    freetype-dev \
    libjpeg-turbo-dev \
    libmcrypt-dev \
    libpng-dev \
    libtool \
    libbz2 \
    bzip2 \
    bzip2-dev \
    libstdc++ \
    libxslt-dev \
    openldap-dev \
    imagemagick-dev \
    make \
    unzip \
    wget && \
    docker-php-ext-install bcmath mcrypt zip bz2 pdo_mysql mysqli simplexml opcache sockets mbstring pcntl xsl && \
    docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ && \
    # pecl install imagick && \
    # docker-php-ext-enable imagick && \
    pecl install redis\
    docker-php-ext-enable redis && \
    pecl install swoole && \
    docker-php-ext-enable swoole && \
    docker-php-ext-install gd && \
    docker-php-ext-enable opcache && \
    apk del build-base \
    linux-headers \
    libaio-dev \
    && rm -rf /var/cache/apk/*

VOLUME /var/www
WORKDIR /var/www

CMD php-fpm