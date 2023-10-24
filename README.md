# Java Microservice
Build an Spring Boot Java Microservice, Dockerize, and Deploy to Kubernetes Cluster
## Prerequisites:

Install Java Development Kit (JDK), Maven, Docker, and Kubernetes on your local development machine.
Set up a Docker Hub account or another container registry Docker Hub, AWS ECR, DOCR to store your Docker images.
Ensure you have kubectl configured to interact with your Kubernetes cluster.

## Setup
Ensure that you have the necessary tools and accounts set up, as mentioned in the prerequisites.

## Clone Application to the Terminal
Clone the spring  microservice application from your version control system. Assuming you are using Git:

```
git clone https://github.com/mohsinrubel/java-microservice-p7.git
cd java-microservice-p7
```
## Build the Application using Maven
Build your Java microservices using Maven:
```
mvn clean install
```
This will build your microservices and create the necessary JAR files.

## Test the Application Locally
Test your microservices locally. Ensure they are running using `` java -jar target/spring-boot-docker.jar `` command as expected and accessible.

 ## Dockerize Each Application Stack
Create a Dockerfile for each microservice to package it into a Docker image. Here's an example Dockerfile for a Spring Boot microservice:

```
FROM openjdk:17
EXPOSE 8080
ADD target/spring-boot-docker.jar spring-boot-docker.jar 
ENTRYPOINT ["java","-jar","/spring-boot-docker.jar"]
```
