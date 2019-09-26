FROM php:7.3-apache AS dev

CMD ["apache2-foreground"]

FROM dev AS composer

RUN apt-get update && apt-get install -y zip unzip
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

CMD ["composer", "update", "--no-plugins", "--no-scripts"]