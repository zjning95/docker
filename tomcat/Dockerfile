FROM docker.io/centos
ADD apache-tomcat-8.0.32.tar.gz /usr/local/
COPY jdk8 /opt/java/
COPY server.xml /usr/local/apache-tomcat-8.0.32/conf/
ENV JAVA_HOME /opt/java/
ENV JRE_HOME /opt/java/jre
EXPOSE 8080
CMD /usr/local/apache-tomcat-8.0.32/bin/catalina.sh run
