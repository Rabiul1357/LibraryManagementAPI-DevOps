# Library Management REST API

A RESTful Library Management System built using Java, Spring Boot, Spring Data JPA, Hibernate and MySQL.

## Technologies Used

- Java 21
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- Postman
- Git and GitHub

## Features

- Book management (Create, Read, Update, Delete)
- Student management (Create, Read, Update, Delete)
- Book issue and return management
- Maximum 3 active books per student
- Automatic available-copy updates
- Overdue book tracking
- Input validation
- Custom exception handling
- REST API testing

## Project Architecture

Controller → Service → Repository → Database

## Database Configuration

1. Create a MySQL database:

```sql
CREATE DATABASE library_management_devops_db;
```

2. Configure your database credentials using environment variables:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/library_management_devops_db
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
```

Set `DB_USERNAME` and `DB_PASSWORD` in your environment before running the application.

## Run the Application

1. Clone the repository.
2. Open the project in Eclipse or IntelliJ IDEA.
3. Configure MySQL credentials.
4. Run the Spring Boot application.

Server URL:

`http://localhost:8090`

## API Endpoints

### Book Management

| Method | Endpoint |
|---|---|
| POST | `/api/books` |
| GET | `/api/books` |
| GET | `/api/books/{id}` |
| PUT | `/api/books/{id}` |
| DELETE | `/api/books/{id}` |
| GET | `/api/books/category/{category}` |

### Student Management

| Method | Endpoint |
|---|---|
| POST | `/api/students` |
| GET | `/api/students` |
| GET | `/api/students/{id}` |
| PUT | `/api/students/{id}` |
| DELETE | `/api/students/{id}` |

### Book Issue Management

| Method | Endpoint |
|---|---|
| POST | `/api/issues/{studentId}/{bookId}` |
| GET | `/api/issues` |
| GET | `/api/issues/student/{studentId}` |
| PUT | `/api/issues/return/{issueId}` |
| GET | `/api/issues/overdue` |

## Exception Handling

- 400 – Bad Request
- 404 – Resource Not Found
- 409 – Duplicate Resource

## Testing

All REST API endpoints were tested using Postman, including validation and exception-handling scenarios.

## Developer

Developed as a practical Spring Boot project.
