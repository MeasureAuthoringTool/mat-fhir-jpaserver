FROM tomcat:9.0.31-jdk11-openjdk
RUN sed -i 's/port="8080"/port="6060"/' /usr/local/tomcat/conf/server.xml
ADD target/hapi-fhir-jpaserver.war /usr/local/tomcat/webapps/
CMD ["catalina.sh", "run"]