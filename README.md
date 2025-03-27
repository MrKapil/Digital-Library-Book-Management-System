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
-  Secure API with Exception Handling

---
## **Tech Stack**
- **Backend:** Java, Spring Boot, REST API
- **Database:** MySQL
- **Build Tool:** Maven
- **Version Control:** Git & GitHub
  

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
| `POST`    | `/users/register`| Register a new user  |

#### EX:- localhost:8080/users/register

---

## SQL Database Schema ##

```sql
CREATE TABLE books (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author VARCHAR(255) NOT NULL,
    category VARCHAR(100) NOT NULL,
    availability BOOLEAN NOT NULL DEFAULT TRUE
);

CREATE TABLE users (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

INSERT INTO books (title, author, category, availability) VALUES
('The Great Gatsby', 'F. Scott Fitzgerald', 'Fiction', TRUE),
('To Kill a Mockingbird', 'Harper Lee', 'Fiction', TRUE),
('1984', 'George Orwell', 'Dystopian', TRUE),
('The Catcher in the Rye', 'J.D. Salinger', 'Classic', TRUE),
('Moby-Dick', 'Herman Melville', 'Adventure', TRUE);

INSERT INTO users (username, password) VALUES
('john_doe', 'securepassword'),
('alice_smith', 'mypassword123');
```

### Sample Data Representation

#### Books Table
| ID | Title                | Author               | Category   | Availability |
|----|----------------------|----------------------|------------|--------------|
|  1 | The Great Gatsby     | F. Scott Fitzgerald  | Fiction    | TRUE         |
|  2 | To Kill a Mockingbird| Harper Lee           | Fiction    | TRUE         |
|  3 | 1984                 | George Orwell        | Dystopian  | TRUE         |
|  4 | The Catcher in the Rye | J.D. Salinger      | Classic    | TRUE         |
|  5 | Moby-Dick            | Herman Melville      | Adventure  | TRUE         |

#### Users Table
| ID | Username   | Password        |
|----|------------|-----------------|
|  1 | john_doe   | securepassword  |
|  2 | alice_smith| mypassword123   |

---

## **Challenges Faced:**
- Ensuring smooth integration between **Spring Boot and MySQL**.
- Managing **database migrations and schema updates** efficiently.
- Handling **exception cases** for API requests.
- Implementing **secure user authentication** without using third-party libraries.
- Optimizing **CRUD operations** for performance and scalability.

## **Potential Improvements:**  
- Implement **password hashing** using **BCrypt** for secure password storage.  
- Use **JWT-based authentication** to secure API endpoints.  
- Add **pagination, sorting, and filtering** for efficient data retrieval.  
- Develop a **React or Angular frontend** for better user experience.  
- Expand **unit and integration testing** to ensure system reliability.

