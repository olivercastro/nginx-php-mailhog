FROM php:7.1-fpm

MAINTAINER Oliver Castro <olivertamboboycastro@gmail.com>

RUN apt-get update \
    && apt-get install -y wget

WORKDIR /mhsendmail

RUN wget https://github.com/mailhog/mhsendmail/releases/download/v0.2.0/mhsendmail_linux_amd64

RUN chmod +x mhsendmail_linux_amd64

RUN mv mhsendmail_linux_amd64 /usr/local/bin/mhsendmail

ADD ./config/php.ini /usr/local/etc/php

WORKDIR /var/www/html

CMD ["php-fpm","-F"]