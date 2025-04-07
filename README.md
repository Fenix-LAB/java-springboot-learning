# Java learning Sprint Boot
## Introduction
This project is a personal exploration of Java programming.

My goal is to create a simple API using Spring Boot and Docker. The API will be a simple CRUD application that allows users to create, read, update, and delete resources.
The resources will be stored in a database, and the API will be built using Spring Boot.

## Prerequisites
- Java 17 or later (java --version)
- Maven 3.6 or later (mvn --version)
- Spring Boot 2.5 or later (spring --version)
- Docker (docker --version)

## How to start a new project
1. Create a new directory for your project.
2. Navigate to the directory in your terminal.
3. Run the following command to create a new Spring Boot project:
   ```bash
   spring init --dependencies=web,data-jpa,postgresql --build=maven --java-version=17 --packaging=jar --extract .
   ```
4. Open the project in your favorite IDE (e.g., IntelliJ IDEA, Eclipse, etc.).
5. Clean and build the project using Maven:
   ```bash
   mvn clean install
   # Or skipping tests
   mvn clean install -DskipTests
   ```
6. Run the application using the following command:
   ```bash
    mvn spring-boot:run
    ```
7. Open your web browser and navigate to `http://localhost:8080` to see the default Spring Boot welcome page.
8. To stop the application, press `Ctrl + C` in the terminal where the application is running.
    
9. Open the `pom.xml` file and add the following dependencies:
   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-data-jpa</artifactId>
   </dependency>
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-web</artifactId>
   </dependency>
   <dependency>
       <groupId>org.postgresql</groupId>
       <artifactId>postgresql</artifactId>
       <scope>runtime</scope>
   </dependency>
   ```

   ## Dependency for a dummy database
   ```xml
   <dependency>
       <groupId>com.h2database</groupId>
       <artifactId>h2</artifactId>
       <scope>runtime</scope>
   </dependency>
   ```
 
 ## DEpendency for hot reloading
   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-devtools</artifactId>
       <scope>runtime</scope>
       <optional>true</optional>
   </dependency>
   ```
   ## Dependency for testing
   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-test</artifactId>
       <scope>test</scope>
   </dependency>
   ```

# Notes (markdown)
![Note]
> ALWAYS use the comand `mvn clean install` to build the project every time you add a new dependency to the `pom.xml` file. This will ensure that all dependencies are downloaded and the project is built correctly.

## Useful commands
- To run the application:
```bash
mvn spring-boot:run
```
- To run the application with Java:
```bash
java -jar target/your-application.jar
```
- To show dependency tree:
```bash
mvn dependency:tree
```
- To run tests:
```bash
mvn test
```
    
