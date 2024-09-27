FROM openjdk:11 AS BUILD
RUN apt update && apt install maven -y
RUN git clone https://github.com/devopshydclub/vprofile-project.git
RUN cd vprofile-project && git checkout docker && maven install

FROM tomcat:9-jre11
RUN rm -rf /urs/local/tomcat/webapps/*
COPY --from=BUILD vprofile-project/target/vprofile-v2.war /urs/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]