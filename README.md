# docker
The company is using dockerfile

docker run -v /webdata:/webdata --name mynginx --link=tomcat-manage:tomcat-manage --link=tomcat-api:tomcat-api -it -p 80:80 mynginx     
启动nginx

docker run --hostname=tomcat-api -v /webdata:/webdata --name tomcat-api  -d -p 9080:8080 tomcat-api      								
启动tomcat-api

docker run --hostname=tomcat-manage -v /webdata:/webdata --name tomcat-manage  -d -p 8080:8080 tomcat-manage      						
启动tomcat-manage 

docker run --hostname tomcat-test -v /data/test/webapps:/usr/local/apache-tomcat-8.0.32/webapps -v /data/test/logs:/usr/local/apache-tomcat-8.0.32/logs --name tomcat-test -d -p 9080:8080 docker.io/zjning1995/tomcat8
