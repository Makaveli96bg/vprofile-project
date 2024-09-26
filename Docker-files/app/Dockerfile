# Stage 1: Build the project with Maven
FROM openjdk:11 AS build_image
RUN apt update && apt install maven -y
RUN git clone https://github.com/Makaveli96bg/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install

# Stage 2: Set up Tomcat and deploy the built WAR file
FROM tomcat:9-jre11 
LABEL "project"="vprofile"
LABEL "Author"="Imran"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build_image /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD [ "catalina.sh", "run" ]
