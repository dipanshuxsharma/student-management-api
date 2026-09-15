# Student Management API

A RESTful Student Management API built using Java, Spring Boot, Spring Data JPA, MySQL, Spring Security, Validation, and Swagger/OpenAPI.

## Features

* Create a student
* Get all students
* Get student by ID
* Update student
* Delete student
* Search students by name
* Pagination
* Sorting
* Request validation
* Custom exception handling
* Swagger/OpenAPI documentation
* MySQL database integration

## Tech Stack

* Java
* Spring Boot
* Spring MVC / REST API
* Spring Data JPA
* Hibernate
* MySQL
* Spring Security
* Jakarta Validation
* Swagger / OpenAPI
* Maven

## API Endpoints

| Method | Endpoint                        | Description                            |
| ------ | ------------------------------- | -------------------------------------- |
| POST   | `/api/students`                 | Create student                         |
| GET    | `/api/students`                 | Get students with pagination & sorting |
| GET    | `/api/students/{id}`            | Get student by ID                      |
| GET    | `/api/students/search?name=Rah` | Search students by name                |
| PUT    | `/api/students/{id}`            | Update student                         |
| DELETE | `/api/students/{id}`            | Delete student                         |

## Pagination & Sorting

Example:

`GET /api/students?page=0&size=5&sortBy=name`

* `page` → Page number
* `size` → Number of students per page
* `sortBy` → Field used for sorting

## Validation

The API validates:

* Name
* Email
* Phone number
* Department
* Age

Invalid requests return HTTP `400 Bad Request`.

## Exception Handling

Custom exception handling is implemented for cases where a student does not exist.

Example:

`GET /api/students/999`

Returns HTTP `404 Not Found`.

## Swagger Documentation

Swagger UI is available at:

`/swagger-ui/index.html`

It can be used to test all API endpoints directly from the browser.

## Database

The application uses MySQL with the database:

`student_management`

## How to Run

1. Clone the repository.
2. Create the `student_management` database in MySQL.
3. Configure MySQL username and password in `application.properties`.
4. Run the Spring Boot application.
5. Open Swagger UI to test the APIs.

## Author

Dipanshu Sharma
