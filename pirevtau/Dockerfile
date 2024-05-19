# docker build -t mosazhaw/djl-serving-consumer .

FROM openjdk:21-jdk-slim

# Copy Files
WORKDIR /usr/src/app
COPY . .

# Install
RUN ./mvnw -Dmaven.test.skip=true package

# Docker Run Command
EXPOSE 8082
CMD ["java","-jar","/usr/src/app/target/consumer-0.0.1-SNAPSHOT.jar"]