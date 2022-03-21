# Buildtime
FROM maven:3.8.4-jdk-8-slim AS builder
WORKDIR app
COPY src .
COPY pom.xml .
RUN mvn clean package

# Runtime
FROM openjdk:11-jre-slim
COPY --from=builder /app/target/multistage-demo-java-1.0.jar /usr/local/lib/multistage-demo.jar
ENTRYPOINT ["java","-jar","/usr/local/lib/multistage-demo.jar"]