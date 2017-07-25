FROM tomcat
# Expose web port
EXPOSE 8080

ENV CATALINA_HOME /usr/local/tomcat
ENV jar /usr/lib/jvm/java-1.8.0-openjdk-amd64/jre/lib/security
COPY server.xml $CATALINA_HOME/conf/
COPY US_export_policy.jar $jar
COPY local_policy.jar $jar

# Launch Tomcat on startup
CMD $CATALINA_HOME/bin/catalina.sh run
