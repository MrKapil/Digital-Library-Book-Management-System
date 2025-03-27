# Digital Library Book Management System

## **Overview**
This is a **Spring Boot + MySQL** project for managing books in a digital library. It provides REST APIs to perform CRUD operations on books and user registration. The system ensures efficient book management and user handling.

---
## **Features**
-  Add, Retrieve, and Delete Books
-  User Registration
-  MySQL Database Integration
-  REST API with Spring Boot
-  API Testing using Postman
-  Easy Deployment on Railway.app
-  Secure API with Exception Handling

---
## **Tech Stack**
- **Backend:** Java, Spring Boot, REST API
- **Database:** MySQL
- **Build Tool:** Maven
- **Version Control:** Git & GitHub
- **Deployment:** Railway.app

---
## **Prerequisites**
Ensure you have the following installed before running the project:
- Java 17 or later
- Maven
- MySQL Server
- Apache Tomcat Server
- Git (for version control)
- Postman (for API testing)

---
## **📂 Project Structure**
```
📦 Digital-Library
├── 📂 src/main/java/com/demo
│   ├── 📂 controller  # REST API Controllers
│   ├── 📂 entity      # Database Entities
│   ├── 📂 repository  # JPA Repositories
│   ├── 📂 service     # Business Logic Layer
│   ├── 📂 exception   # Custom Exception Handling
├── 📂 src/main/resources
│   ├── application.properties  # Database Configuration
├── 📂 target  # Compiled files after build
├── pom.xml  # Maven Dependencies
├── README.md  # Documentation with Database Schema
```

---
## **Setup & Installation**
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/YOUR_GITHUB_USERNAME/Digital-Library.git
cd Digital-Library
```

### **2️⃣ Configure Database**
spring.application.name=DigitalLibraryBookManagementSystem

### Remote MySQL Database Properties
- spring.datasource.url=jdbc:mysql://sql12.freesqldatabase.com:3306/sql12769892

- spring.datasource.username=sql12769892

- spring.datasource.password=3TKQGyh8KE

### Hibernate Properties
- spring.jpa.hibernate.ddl-auto=update

- spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

### Server Port Configuration
- server.port=8080

### **3️⃣ Run the Application**

-mvn spring-boot:run

#### The app will start on **http://localhost:8080**

---
## **API Endpoints**
### **Book Management**
| Method   |   Endpoint    | Description    |
|----------|---------------|----------------|
| `GET`    | `/books`      | Get all books  |
| `GET`    | `/books/{id}` | Get book by ID |
| `POST`   | `/books`      | Add a new book |
| `DELETE` | `/books/{id}` | Delete book    |

#### EX:-localhost:8080/books

### **User Management**
|  Method   |     Endpoint     |  Description         |
|-----------|------------------|----------------------|
| `john_doe`| `/users/register`| Register a new user  |

#### EX:- localhost:8080/users/register
