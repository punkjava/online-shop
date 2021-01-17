FROM php:7.3.3-apache
RUN apt-get update && apt-get upgrade -y && docker-php-ext-install mysqli && rm -rf /var/lib/apt/lists/*
EXPOSE 80
