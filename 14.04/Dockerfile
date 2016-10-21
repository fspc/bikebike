FROM ubuntu:14.04
MAINTAINER Jonathan Rosenbaum <gnuser@gmail.com> 

# Not all applications use mysql, but nevertheless.
RUN echo "mysql-server-5.5 mysql-server/root_password password" | debconf-set-selections; echo "mysql-server-5.5 mysql-server/root_password_again password" | debconf-set-selections; apt-get update && apt-get -y install mysql-server git supervisor ruby make libmysqlclient-dev ruby-dev 

COPY supervisord.conf /etc/supervisor/supervisord.conf
