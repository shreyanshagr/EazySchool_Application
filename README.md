# EazySchool Application - README

## Overview

EazySchool is a comprehensive web application designed to manage and streamline the administrative tasks of a school. The application provides features like contact management, holiday management, user authentication, dashboard displays, and global exception handling. This README provides detailed information on the application's structure, dependencies, and usage.

## Table of Contents

1. [Technologies Used](#technologies-used)
2. [Project Structure](#project-structure)
3. [Dependencies](#dependencies)
4. [Installation](#installation)
5. [Configuration](#configuration)
6. [Running the Application](#running-the-application)
7. [Features](#features)
8. [Contributing](#contributing)
9. [License](#license)

## Technologies Used

- Java
- Spring Boot
- Spring MVC
- Spring Security
- Spring Data JPA
- Thymeleaf
- Lombok
- H2 Database
- JDBC Template
- SLF4J

## Project Structure

```plaintext
src
├── main
│   ├── java
│   │   └── com
│   │       └── eazybytes
│   │           └── eazyschool
│   │               ├── controller
│   │               ├── model
│   │               ├── repository
│   │               ├── rommappers
│   │               └── service
│   └── resources
│       ├── static
│       ├── templates
│       └── application.properties
└── test
    └── java
        └── com
            └── eazybytes
                └── eazyschool
```

### Directories and Files

- `controller`: Contains Spring MVC controllers for handling web requests.
- `model`: Contains entity classes representing the application's data model.
- `repository`: Contains repository classes for data access.
- `rommappers`: Contains row mappers for JDBC operations.
- `service`: Contains service classes for business logic.
- `static`: Contains static assets like CSS, JavaScript, and images.
- `templates`: Contains Thymeleaf templates for the views.
- `application.properties`: Configuration properties for the application.

## Dependencies

The application uses the following dependencies:

- Spring Boot Starter Web
- Spring Boot Starter Thymeleaf
- Spring Boot Starter Data JPA
- Spring Boot Starter Security
- Spring Boot Starter JDBC
- Lombok
- H2 Database
- SLF4J

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/eazybytes/eazyschool.git
   cd eazyschool
   ```

2. **Build the project:**
   ```bash
   ./mvnw clean install
   ```

## Configuration

The application uses the `application.properties` file for configuration. By default, it is set up to use an H2 in-memory database. You can modify this configuration to connect to a different database if needed.

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
spring.jpa.hibernate.ddl-auto=update
```

## Running the Application

1. **Run the application:**
   ```bash
   ./mvnw spring-boot:run
   ```

2. **Access the application:**
   Open a web browser and navigate to `http://localhost:8080`.

## Features

### Contact Management

- Display contact page: `/contact`
- Save contact message: `/saveMsg` (POST)
- Display messages: `/displayMessages`
- Close message: `/closeMsg` (GET)

### User Authentication

- Login: `/login`
- Logout: `/logout`

### Dashboard

- Display dashboard: `/dashboard`

### Holiday Management

- Display holidays: `/holidays/{display}`

### Global Exception Handling

- Handle exceptions globally: Configured in `GlobalExceptionController`

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

---

Thank you for using EazySchool! For any questions or feedback, please contact the repository maintainer.
