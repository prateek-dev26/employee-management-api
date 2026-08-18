# 🚀 Employee Management API

A production-style **RESTful Employee Management API** built using **Java, Spring Boot, Spring Data JPA, and MySQL**.

The application provides complete CRUD operations for employee management and includes **Swagger/OpenAPI documentation**, **Docker containerization**, and **Docker Compose** for running the Spring Boot application with MySQL.

---

## ✨ Features

* ✅ Create employee
* ✅ Get all employees
* ✅ Get employee by ID
* ✅ Update employee details
* ✅ Delete employee
* ✅ RESTful API architecture
* ✅ Request validation
* ✅ Global exception handling
* ✅ MySQL database integration
* ✅ Spring Data JPA / Hibernate
* ✅ Swagger/OpenAPI documentation
* ✅ Docker containerization
* ✅ Docker Compose
* ✅ Environment-based database credentials

---

## 🛠️ Tech Stack

| Technology            | Purpose                     |
| --------------------- | --------------------------- |
| **Java 17**           | Programming Language        |
| **Spring Boot**       | Backend Framework           |
| **Spring Data JPA**   | Database Access             |
| **Hibernate**         | ORM                         |
| **MySQL 8**           | Relational Database         |
| **Maven**             | Build Tool                  |
| **Swagger / OpenAPI** | API Documentation           |
| **Docker**            | Containerization            |
| **Docker Compose**    | Multi-container Environment |
| **Git & GitHub**      | Version Control             |

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │      Client         │
                    │ Postman / Swagger   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Spring Boot API   │
                    │                     │
                    │ EmployeeController  │
                    │ EmployeeService     │
                    │ EmployeeRepository  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       MySQL         │
                    │    employee_db      │
                    └─────────────────────┘
```

---

## 📂 Project Structure

```text
employee-management-api/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── employee_management_api/
│   │   │       ├── config/
│   │   │       ├── controller/
│   │   │       ├── entity/
│   │   │       ├── exception/
│   │   │       ├── repository/
│   │   │       └── service/
│   │   │
│   │   └── resources/
│   │       └── application.properties
│   │
│   ├── screenshots/
│   │   ├── swagger.png
│   │   └── docker.png
│   │
│   └── test/
│
├── Dockerfile
├── docker-compose.yml
├── pom.xml
├── .gitignore
└── README.md
```

---

## 🔗 REST API Endpoints

| Method   | Endpoint          | Description           |
| -------- | ----------------- | --------------------- |
| `POST`   | `/employees`      | Create a new employee |
| `GET`    | `/employees`      | Get all employees     |
| `GET`    | `/employees/{id}` | Get employee by ID    |
| `PUT`    | `/employees/{id}` | Update employee       |
| `DELETE` | `/employees/{id}` | Delete employee       |

### Example Employee JSON

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "department": "IT",
  "salary": 50000
}
```

---

## 📖 Swagger / OpenAPI

Swagger UI provides interactive API documentation and allows the REST endpoints to be tested directly from the browser.

When the application is running:

```text
http://localhost:8080/swagger-ui/index.html
```

### Swagger UI

---

## 🗄️ Database

The application uses **MySQL** with **Spring Data JPA and Hibernate**.

Database:

```text
Database: employee_db
```

Database configuration is stored in:

```text
src/main/resources/application.properties
```

### 🔐 Environment Variables

Database credentials are **not hardcoded** in the application configuration.

The application uses:

```properties
spring.datasource.username=${MYSQL_USERNAME}
spring.datasource.password=${MYSQL_PASSWORD}
```

For local development, create a `.env` file:

```env
MYSQL_USERNAME=root
MYSQL_PASSWORD=your_password
```

> ⚠️ `.env` is excluded from Git using `.gitignore`. Never commit database passwords or other secrets to GitHub.

---

# 💻 Run Locally

## Prerequisites

Make sure the following are installed:

* Java 17+
* Maven
* MySQL
* Git

---

## 1. Clone the Repository

```bash
git clone https://github.com/prateek-dev26/employee-management-api.git
```

```bash
cd employee-management-api
```

---

## 2. Configure Database

Create the MySQL database:

```sql
CREATE DATABASE employee_db;
```

Set your database credentials using environment variables.

Example:

```text
MYSQL_USERNAME=root
MYSQL_PASSWORD=your_password
```

---

## 3. Build the Application

```bash
mvn clean package
```

---

## 4. Run the Application

```bash
mvn spring-boot:run
```

The application will start on:

```text
http://localhost:8080
```

Swagger UI:

```text
http://localhost:8080/swagger-ui/index.html
```

---

# 🐳 Run Using Docker

## Build Docker Image

```bash
docker build -t employee-management-api .
```

## Run Docker Container

```bash
docker run -p 8080:8080 employee-management-api
```

The API will be available at:

```text
http://localhost:8080
```

---

# 🐳 Docker Compose

Docker Compose runs the **Spring Boot application and MySQL database together**.

## 1. Create `.env`

Create a `.env` file in the project root:

```env
MYSQL_USERNAME=root
MYSQL_PASSWORD=your_password
```

> Do not commit this file to GitHub.

## 2. Start Services

```bash
docker compose up -d
```

## 3. Check Containers

```bash
docker compose ps
```

## 4. View Application Logs

```bash
docker compose logs -f employee-management-api
```

## 5. Rebuild and Start

```bash
docker compose up -d --build
```

## 6. Stop Services

```bash
docker compose down
```

---

## 📸 Docker Containers

The Spring Boot application and MySQL database can be run together using Docker Compose.

---

## 📸 Swagger UI

Interactive API documentation provided through Swagger/OpenAPI.

---

## 🔮 Future Enhancements

* 🔐 Spring Security
* 🔑 JWT-based authentication
* 👥 Role-based authorization
* 📄 Pagination and sorting
* 🔎 Employee search and filtering
* 🧪 More unit and integration tests
* 🔄 CI/CD pipeline using Jenkins or GitHub Actions
* ☁️ AWS deployment

---

## 👨‍💻 Author

### Prateek Vishwakarma

**Java Full Stack Developer | DevOps Engineer**

GitHub:
https://github.com/prateek-dev26

LinkedIn:
https://www.linkedin.com/in/prateekvishw-dev

---

## ⭐ Support

If you find this project useful, consider giving it a ⭐ on GitHub.
