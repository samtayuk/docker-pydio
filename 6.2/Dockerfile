FROM samtayuk/nginx-php:php7
MAINTAINER Samuel Taylor "samtaylor.uk@gmail.com"

ENV PYDIO_VERSION 6.2.2


RUN cd /app \
    && wget -qO- wget http://downloads.sourceforge.net/project/ajaxplorer/pydio/stable-channel/${PYDIO_VERSION}/pydio-core-${PYDIO_VERSION}.tar.gz | tar xz \
    && mv pydio-core-${PYDIO_VERSION} pydio-core \
    && chown -R www-data:www-data /app/pydio-core

COPY php.ini /etc/php/7.0/fpm/conf.d/50-custom.ini

COPY default.conf /etc/nginx/conf.d/
