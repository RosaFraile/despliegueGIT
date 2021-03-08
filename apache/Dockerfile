FROM ubuntu:18.04

RUN apt-get update && apt-get install -y apache2 \
    && apt-get -y install libapache2-mod-fcgid \
    && a2enmod proxy_fcgi \
    && apt-get -y install git \
    && git clone https://github.com/deaw-birt/despliegue-PHP.git \
    && mv /despliegue-PHP/php/*.* /var/www/html/

COPY 000-default.conf /etc/apache2/sites-available
EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]