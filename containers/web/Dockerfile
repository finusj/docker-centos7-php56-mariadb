FROM centos:7

MAINTAINER Luiz Fumes <lcfumes@gmail.com>

RUN yum -y update && yum clean all

ADD nginx.repo /etc/yum.repos.d/nginx.repo
#ADD mariadb.repo /etc/yum.repos.d/mariadb.repo

RUN yum -y install nginx && yum clean all 

RUN yum -y --enablerepo=remi,remi-php56 install nginx php-fpm php-common

#RUN yum -y install mariadb && yum clean all

RUN yum install -y python-setuptools
RUN easy_install pip
RUN pip install supervisor 

# Adding the configuration file of the nginx
ADD nginx.conf /etc/nginx/nginx.conf
ADD web.conf /etc/nginx/conf.d/default.conf

# Adding the configuration file of the Supervisor
ADD supervisord.conf /etc/

# Set the port to 80 
EXPOSE 80

# Executing supervisord
CMD ["supervisord", "-n"]
