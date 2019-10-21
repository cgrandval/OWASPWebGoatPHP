FROM php:5.6-apache-stretch

ENV PROJECT_DIR /var/www/project

WORKDIR $PROJECT_DIR

RUN a2enmod rewrite \
 && sed -i "s|DocumentRoot /var/www/html|DocumentRoot ${PROJECT_DIR}|" /etc/apache2/sites-available/000-default.conf \
 && docker-php-ext-install pdo pdo_mysql
