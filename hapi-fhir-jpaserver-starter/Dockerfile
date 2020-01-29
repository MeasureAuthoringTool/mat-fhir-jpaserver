FROM tomcat:9-jre8
ARG WAR_FILE=target/hapi-fhir-jpaserver.war
RUN mkdir -p /data/hapi/lucenefiles && chmod 775 /data/hapi/lucenefiles
COPY ${WAR_FILE} /usr/local/tomcat/webapps/

EXPOSE 8080

CMD ["catalina.sh", "run"]