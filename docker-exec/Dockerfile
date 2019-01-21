FROM gmaslowski/jdk:8

VOLUME /tmp
ARG JAR_FILE
ADD ${JAR_FILE} app.jar

ENTRYPOINT ["java", "-XX:+ExitOnOutOfMemoryError", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/app.jar"]