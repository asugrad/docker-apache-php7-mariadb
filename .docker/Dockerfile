FROM php:7.2.7-apache

MAINTAINER Michael ONeil

COPY . /var/www/html
COPY .docker/vhost.conf /etc/apache2/sites-available/000-default.conf

RUN chown -R www-data:www-data /var/www/html \
    && a2enmod rewrite

#RUN chmod -R o+rw /var/www/html/bootstrap/ /var/www/html/storage/

RUN docker-php-ext-install mbstring pdo pdo_mysql \
    && chown -R www-data:www-data /var/www/html