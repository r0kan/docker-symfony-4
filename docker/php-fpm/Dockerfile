FROM phpdockerio/php72-fpm:latest
WORKDIR /app

RUN apt-get update \
    # Install selected extensions and other stuff
    && apt-get -y --no-install-recommends install  php7.2-mysql \
    # Install git
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
RUN usermod -u 1000 www-data
