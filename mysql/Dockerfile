FROM pangliang/ubuntu
MAINTAINER pangliang "418094911@qq.com"

# mysql
RUN \
	echo "mysql-server-5.5 mysql-server/root_password_again password xm123456" | debconf-set-selections && \
	echo "mysql-server-5.5 mysql-server/root_password password xm123456" | debconf-set-selections && \
	apt-get install -y mysql-server
ADD my.cnf /etc/mysql/my.cnf
ADD init-mysql.sql /init-mysql.sql

ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf


# Expose ports.
EXPOSE 3306
