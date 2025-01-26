# Start with a base image containing Java runtime
FROM openjdk:17-jdk-slim

# Add the application's jar to the image
COPY target/*.jar microservice.jar

RUN apt-get update && apt-get install -y curl

EXPOSE 80

# Command to execute the application
ENTRYPOINT ["java", "-jar", "microservice.jar"]