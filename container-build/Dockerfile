# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"

RUN sed -i 's/isten 80/isten 8080/g/' /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/run/httpd /var/log/httpd \
&&  chmod -R g=u /var/run/httpd /var/log/httpd

USER 1001

