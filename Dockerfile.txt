FROM centos:latest
LABEL maintainer="Academy"
RUN yum -y install httpd
COPY index.html /var/www/html/
COPY dog-*.jpg /var/www/html/
ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
EXPOSE 80