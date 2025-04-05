# Use Tomcat 9 image with Java 17 (compatible with Spring Boot 2.7.x)
FROM tomcat:9.0.85-jdk17

MAINTAINER "Akash Verma"

# Optional: environment variables for DB (can also be set via application.properties)
ENV JLC_MYSQL_HOST=jlc-mysql
ENV JLC_MYSQL_PORT=3306
ENV JLC_MYSQL_DATABASE=bookstoredb
ENV JLC_MYSQL_USER=akash
ENV JLC_MYSQL_PASSWORD=Akash87970@#

# Clean existing webapps
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy your WAR file to webapps folder of Tomcat
COPY target/myjlcapp.war /usr/local/tomcat/webapps/ROOT.war

# Expose default Tomcat port
EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]
