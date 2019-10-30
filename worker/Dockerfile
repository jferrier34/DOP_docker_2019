FROM maven:3.5-jdk-8-alpine AS builder
WORKDIR /usr/worker
COPY . .
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
WORKDIR /usr/worker
COPY --from=0 /usr/worker .
CMD [ "java", "-jar", "target/worker-jar-with-dependencies.jar" ]