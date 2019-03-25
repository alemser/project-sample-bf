FROM adoptopenjdk/openjdk11

COPY backend /opt/app
COPY frontend /opt/app
COPY gradle /opt/app
COPY build.gradle /opt/app
COPY settings.gradle /opt/app
COPY gradlew /opt/app

RUN /opt/app/gradlew
RUN mv backend/build/libs/backend-*.jar /opt/app/app.jar

ENV JAVA_OPTS="${JAVA_OPTS} -Xms512m -Xmx512m"

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/opt/app/app.jar"]
