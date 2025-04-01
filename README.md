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
   spring init --dependencies=web,data-jpa,postgresql --build=maven --java-version=17 --packaging=jar --name=my-api my-api
   ```
4. Navigate to the newly created project directory:
   ```bash
   cd my-api
   ```
5. Open the project in your favorite IDE (e.g., IntelliJ IDEA, Eclipse, etc.).
6. Open the `pom.xml` file and add the following dependencies:
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
7. Create a new file named `application.properties` in the `src/main/resources` directory and add the following configuration:
   ```properties
    spring.datasource.url=jdbc:postgresql://localhost:5432/mydb
    spring.datasource.username=myuser
    spring.datasource.password=mypassword
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
    spring.jpa.properties.hibernate.format_sql=true
    spring.jpa.properties.hibernate.use_sql_comments=true


    
