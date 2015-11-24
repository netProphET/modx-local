FROM nmcteam/php56
MAINTAINER Michael Schell <mike@webprogramming.ca>

CMD ["/sbin/my_init"]

RUN usermod -u 1000 www-data

RUN apt-get update && apt-get install -y zip

RUN apt-get install -y --force-yes php5-imagick

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=bin --filename=composer

RUN sed -i 's/;date\.timezone.*/date.timezone = UTC/' /etc/php5/fpm/php.ini
RUN sed -i 's/;date\.timezone.*/date.timezone = UTC/' /etc/php5/cli/php.ini

ADD http://modx.s3.amazonaws.com/releases/teleport/teleport.phar /usr/local/bin/
RUN chmod 777 /usr/local/bin/teleport.phar
RUN ln -s /usr/local/bin/teleport.phar /usr/local/bin/teleport
