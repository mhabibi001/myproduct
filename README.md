# My Product Backend
This is the backend service for My Product. It provides RESTful endpoints to list and create products, and is intended 
to be used with the My Product React frontend.

## Features

- REST API for managing products
- PostgreSQL database integration
- Swagger UI documentation

---

## Tech Stack

- Java 17
- Spring Boot 3.5
- Spring Data JPA
- PostgreSQL
- Swagger/OpenAPI (SpringDoc)
- Maven

---

## Getting Started

### Prerequisites
- Java 17
- Maven 3.x
- PostgreSQL

### Installation

1. Clone the repository:
```bash
   git clone https://github.com/mhabibi001/myproduct.git
   cd myproduct
```

2. `application.yml`
Make sure your local Postgres is running with the correct credentials:

```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/myproducts
    username: username
    password: password
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: false
    properties:
      hibernate:
        format_sql: true
```

3. Compiling the Application
```bash
mvn clean install
```

4. Running the Application
```bash
mvn spring-boot:run
```

## API Documentation
Once the app is running, Swagger UI is available at:

http://localhost:8080/swagger-ui.html

## CORS Configuration
This backend allows CORS from:

`http://localhost:3000 (React frontend)`

If you change the frontend domain, update it in WebConfig.java.

