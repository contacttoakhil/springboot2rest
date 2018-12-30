# springboot2rest
This is a simple Spring Boot 2.0 Application which expose a simple rest API based on Spring JPA. It uses JDK 11 and Docker.

## Running Spring Boot Application
There are various ways to [run](https://dzone.com/articles/five-ways-of-running-spring-boot-application) spring boot applications.

## Running via maven plugin
mvn spring-boot:run

## Package into executable jar
mvn clean install package

## Deploying into Docker container
1. Create executable jar
2. Build image: docker build -t spring-boot2-docker .
3. Run the image: docker run -p 8085:8085 spring-boot2-docker

## Deploying into Docker container using docker-compose
1. Create executable jar using 'mvn clean package'
2. Create image and deploy in container using 'docker-compose up -d'
3. Then you can check docker container info using 'docker ps'

## Testing via postman: 
GET:http://localhost:8085/employees
