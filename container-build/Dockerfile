# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.description=" hola puerto 8080"


RUN sed -i "s/LISTEN 80/LISTEN 8080/g" /etc/httpd/conf/httpd.conf \
        && chgrp -R 0 /var/log/httpd /var/run/httpd \
	&& chmod -R g=u /var/logs/httpd /var/httpd/bin

EXPOSE 8080

USER 1001

