FROM java:8-jre

ENV mycat-version Mycat-server-1.6-RELEASE-20161028204710-linux.tar.gz
USER root
COPY ./Mycat-server-1.6-RELEASE-20161028204710-linux.tar.gz /
RUN tar -zxf /Mycat-server-1.6-RELEASE-20161028204710-linux.tar.gz
ENV MYCAT_HOME=/mycat
ENV PATH=$PATH:$MYCAT_HOME/bin

COPY schema.xml /mycat/conf/schema.xml
COPY server.xml /mycat/conf/server.xml
COPY log4j2.xml /mycat/conf/log4j2.xml

WORKDIR $MYCAT_HOME/bin
RUN chmod u+x ./mycat
EXPOSE 8066 9066
CMD ["./mycat","console"]
