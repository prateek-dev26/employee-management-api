# Employee Management API

A RESTful Employee Management API built using **Java, Spring Boot, Spring Data JPA, and MySQL**. The application provides CRUD operations for managing employee records and is integrated with **Swagger/OpenAPI** for API documentation and **Docker/Docker Compose** for containerization.

## 🚀 Features

* Create new employees
* Retrieve all employees
* Retrieve employee by ID
* Update employee details
* Delete employees
* RESTful API architecture
* MySQL database integration
* Spring Data JPA and Hibernate
* Swagger/OpenAPI documentation
* Docker containerization
* Docker Compose support

## 🛠️ Tech Stack

| Technology        | Purpose                     |
| ----------------- | --------------------------- |
| Java              | Programming Language        |
| Spring Boot       | Backend Framework           |
| Spring Data JPA   | Database Access             |
| Hibernate         | ORM                         |
| MySQL             | Relational Database         |
| Maven             | Build Tool                  |
| Swagger / OpenAPI | API Documentation           |
| Docker            | Containerization            |
| Docker Compose    | Multi-container Environment |
| Git & GitHub      | Version Control             |

## 📂 Project Structure

```text
employee-management-api/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── ...
│   │   └── resources/
│   │       └── application.properties
│   │
│   └── test/
│
├── screenshots/
│   ├── swagger.png
│   └── docker.png
│
├── Dockerfile
├── docker-compose.yml
├── pom.xml
└── README.md
```

## 🔗 API Endpoints

| Method | Endpoint          | Description           |
| ------ | ----------------- | --------------------- |
| GET    | `/employees`      | Get all employees     |
| GET    | `/employees/{id}` | Get employee by ID    |
| POST   | `/employees`      | Create a new employee |
| PUT    | `/employees/{id}` | Update employee       |
| DELETE | `/employees/{id}` | Delete employee       |

> Update the endpoint paths above if your controller uses a different base URL.

## 📖 Swagger API Documentation

Swagger/OpenAPI is integrated into the project to provide interactive API documentation and testing.

When the application is running, open:

```text
http://localhost:8080/swagger-ui/index.html
```

### Swagger UI

## 🗄️ Database

The application uses **MySQL** as the relational database and **Spring Data JPA/Hibernate** for database operations.

Database configuration is maintained in:

```text
src/main/resources/application.properties
```

When running with Docker Compose, the Spring Boot application connects to the MySQL container through the Docker network.

## 💻 Run Locally

### Prerequisites

Make sure the following are installed:

* Java 17 or compatible version
* Maven
* MySQL
* Git

### 1. Clone the Repository

```bash
git clone https://github.com/prateek-dev26/employee-management-api.git
```

```bash
cd employee-management-api
```

### 2. Create the Database

Create the MySQL database:

```sql
CREATE DATABASE employee_db;
```

Configure your MySQL username, password, and database settings in:

```text
src/main/resources/application.properties
```

### 3. Build the Application

```bash
mvn clean package
```

### 4. Run the Application

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

## 🐳 Run Using Docker

### Build Docker Image

```bash
docker build -t employee-management-api .
```

### Run Docker Container

```bash
docker run -p 8080:8080 employee-management-api
```

The API will be available at:

```text
http://localhost:8080
```

## 🐳 Docker Compose

The project supports Docker Compose for running the **Spring Boot application and MySQL database together**.

### Start Services

```bash
docker compose up -d
```

### Check Running Containers

```bash
docker compose ps
```

### View Logs

```bash
docker compose logs -f employee-management-api
```

### Rebuild and Start

```bash
docker compose up -d --build
```

### Stop Services

```bash
docker compose down
```

## 📸 Docker Containers

The application and MySQL database are successfully running using Docker Compose.

## 📸 Swagger UI

Interactive API documentation provided through Swagger/OpenAPI.

## 🔮 Future Enhancements

* Add Spring Security
* Implement JWT-based authentication
* Add role-based authorization
* Add pagination and sorting
* Add employee search and filtering
* Add unit and integration testing
* Add CI/CD pipeline using Jenkins or GitHub Actions
* Deploy the application to AWS

## 👨‍💻 Author

**Prateek Vishwakarma**

Java Full Stack Developer | DevOps Enthusiast

**GitHub:**
https://github.com/prateek-dev26

**LinkedIn:**
https://www.linkedin.com/in/prateekvishw

## ⭐ Support

If you find this project useful, consider giving it a ⭐ on GitHub.
