# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080
LABEL io.openshift.expose.services="8080:http" \
      io.k8s.description"sample"
      io.k8s.displayname="somthing"
      io.openshift.tags="apache"
RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp 0 -R /var/log/httpd /var/run/httpd && 
    chmod -R g=u /var/log/httpd /var/run/httpd
USER 1001
