FROM adoptopenjdk/openjdk11

COPY backend/build/libs/backend-*.jar app.jar

ENV JAVA_OPTS="${JAVA_OPTS} -Xms512m -Xmx512m"

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
