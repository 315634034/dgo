FROM maven
ADD settings.xml /usr/share/maven/conf
WORKDIR /app
RUN git clone https://github.com/315634034/dgo.git
WORKDIR dgo
RUN git checkout test
RUN mvn package
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "target/dgo-1.0.0.jar"]

