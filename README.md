# springboot2rest
This is a simple [Spring Boot 2.0](https://spring.io/blog/2018/11/30/spring-boot-2-1-1-available-now) Application which expose a simple rest API using in-memory database [H2](https://en.wikipedia.org/wiki/H2_(DBMS)) and [Spring JPA](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/). It uses [JDK 11](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html) and [Docker](https://www.docker.com/).

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
