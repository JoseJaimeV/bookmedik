FROM php:8.3.14-apache

RUN apt-get update && apt-get install -y mariadb-client libmariadb-dev && docker-php-ext-install mysqli


COPY . /var/www/html

WORKDIR /var/www/html



RUN chown -R www-data:www-data /var/www/html && chmod -R 755 /var/www/html


COPY script.sh /usr/local/bin/script.sh
RUN chmod +x /usr/local/bin/script.sh


CMD ["bash", "/usr/local/bin/script.sh"]
