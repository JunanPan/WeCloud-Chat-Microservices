# Use the Maven JDK 8 slim image as the parent image
FROM maven:3.8.4-jdk-8-slim AS build

# Set the working directory in the container
WORKDIR /app

# Copy the pom.xml file and source code into the container
COPY pom.xml .
COPY src ./src

# Compile the application and package it as a JAR file
RUN mvn clean package -DskipTests

# Use OpenJDK 8 JRE slim image to run the JAR file
FROM openjdk:8-jre-slim

EXPOSE 8080

# Copy the JAR file from the build stage into this new stage
COPY --from=build /app/target/*.jar /group-chat-service.jar


# Command to run the application
CMD ["java", "-jar", "/group-chat-service.jar"]
