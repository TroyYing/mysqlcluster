FROM centos:6.9
RUN yum install -y wget
RUN wget https://github.com/Qihoo360/Atlas/releases/download/2.2.1/Atlas-2.2.1.el6.x86_64.rpm
RUN rpm -i Atlas-2.2.1.el6.x86_64.rpm
CMD /usr/local/mysql-proxy/bin/mysql-proxyd test start
