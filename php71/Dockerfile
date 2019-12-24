# Pull base image.
FROM nurettintopal/docker-php:php-7.1

MAINTAINER Nurettin Topal "nurettintopal@gmail.com"

RUN rm -rf /etc/nginx/sites-available/default
RUN rm -rf /etc/nginx/sites-enabled/default

COPY nginx.conf /etc/nginx/sites-available/nginx.conf
WORKDIR /etc/nginx/sites-enabled/
RUN ln -s /etc/nginx/sites-available/nginx.conf /etc/nginx/sites-enabled/nginx.conf

RUN rm -rf /var/www/html
RUN rm -rf /var/www/index.php

COPY . /var/www/app/
WORKDIR /var/www/app

EXPOSE 8080
