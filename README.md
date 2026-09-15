# Student Management API

A **RESTful Student Management API** built with Java and Spring Boot. This project demonstrates core backend development concepts including REST API development, CRUD operations, database integration, pagination, sorting, validation, exception handling, and API documentation.

## 🚀 Features

* Create a student
* Get all students
* Get student by ID
* Update student
* Delete student
* Search students by name
* Pagination
* Sorting
* Request validation
* Global exception handling
* MySQL database integration
* Spring Security integration
* Swagger/OpenAPI documentation

## 🛠️ Tech Stack

* **Java**
* **Spring Boot**
* **Spring MVC / REST API**
* **Spring Data JPA**
* **Hibernate**
* **MySQL**
* **Spring Security**
* **Jakarta Validation**
* **Swagger / OpenAPI**
* **Maven**

## 🏗️ Project Architecture

The application follows a layered backend architecture:

```text
Client
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
MySQL Database
```

### Layers

* **Controller** – Handles HTTP requests and API endpoints.
* **Service** – Contains business logic.
* **Repository** – Performs database operations using Spring Data JPA.
* **Entity** – Represents the database table.
* **Exception Handler** – Handles application exceptions and returns meaningful HTTP responses.

## 📌 API Endpoints

| Method   | Endpoint                        | Description                              |
| -------- | ------------------------------- | ---------------------------------------- |
| `POST`   | `/api/students`                 | Create a new student                     |
| `GET`    | `/api/students`                 | Get students with pagination and sorting |
| `GET`    | `/api/students/{id}`            | Get student by ID                        |
| `GET`    | `/api/students/search?name=Rah` | Search students by name                  |
| `PUT`    | `/api/students/{id}`            | Update student                           |
| `DELETE` | `/api/students/{id}`            | Delete student                           |

## 📄 Pagination & Sorting

The API supports pagination and sorting using query parameters.

### Example

```http
GET /api/students?page=0&size=5&sortBy=name
```

### Parameters

| Parameter | Description                 |
| --------- | --------------------------- |
| `page`    | Page number                 |
| `size`    | Number of students per page |
| `sortBy`  | Field used for sorting      |

## 🔍 Search

Students can be searched by name.

### Example

```http
GET /api/students/search?name=Rah
```

This returns students whose names match the provided search value.

## ✅ Validation

The API validates incoming student data including:

* Name
* Email
* Phone number
* Department
* Age

Invalid requests return:

```text
HTTP 400 Bad Request
```

## ⚠️ Exception Handling

Global exception handling is implemented to provide appropriate HTTP responses for errors.

For example, when a student does not exist:

```http
GET /api/students/999
```

The API returns:

```text
HTTP 404 Not Found
```

## 🔐 Security

Spring Security is integrated into the application for API security.

> If JWT authentication is implemented later, authentication and authorization details can be added here.

## 📚 Swagger / OpenAPI

Swagger/OpenAPI is used to document and test the REST APIs directly from the browser.

After starting the application, open:

```text
http://localhost:8080/swagger-ui/index.html
```

Swagger UI allows you to explore and test the available API endpoints.

## 🗄️ Database

The application uses **MySQL** as the relational database.

Database:

```text
student_management
```

Configure your database credentials in:

```text
src/main/resources/application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_management
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
```

**Do not upload real database passwords or sensitive credentials to GitHub.**

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Create the database

Open MySQL and run:

```sql
CREATE DATABASE student_management;
```

### 3. Configure database

Update your MySQL username and password in:

```text
application.properties
```

### 4. Build the project

```bash
mvn clean install
```

### 5. Run the application

```bash
mvn spring-boot:run
```

You can also run the application directly from your IDE.

### 6. Open Swagger

Once the application starts, visit:

```text
http://localhost:8080/swagger-ui/index.html
```

## 📦 Example Request

### C



