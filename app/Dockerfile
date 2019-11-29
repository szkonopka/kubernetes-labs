FROM openjdk:8

RUN mkdir /myapp &&\
    git clone https://github.com/gstala/app /myapp &&\
    cd /myapp &&\
    chmod a+x ./mvnw &&\
    ./mvnw package -DskipTests -Dspring.profiles.active=container

EXPOSE 8080

CMD java -jar /myapp/target/app-0.0.1-SNAPSHOT.jar -Dspring.profiles.active=container
