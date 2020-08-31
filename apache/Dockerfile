FROM Ubuntu 18.04
MAINTAINER Douglas Rezende Paulo <douglas.rezende@engenharia.ufjf.br>
RUN apt-get update && apt-get install -y apache2  && apt-get clean
ENV APACHE_LOCK_DIR="/var/lock"
ENV APACHE_PID_FILE="/var/run/apache2.pid"
ENV APACHE_RUN_USER="www-data"
ENV APACHE_RUN_GROUP="www-data"
ENV APACHE_LOG_DIR="/var/log/apache2"
LABEL Description="Apache Webserver - Debian - v1.0"
EXPOSE 80
ADD /home/douglas/12444.jpg /var/www/html/
RUN chown -R www-data: /var/www/html/.
CMD /etc/init.d/apache2 start && /bin/bash
