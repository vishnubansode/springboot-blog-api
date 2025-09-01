# 📝 Spring Boot Blog REST API

A Blog Application backend built with **Spring Boot**, providing secure REST APIs for user authentication, post management, categories, and comments.  
This project uses **JWT authentication**, **role-based access control**, **pagination & sorting**, and **Swagger OpenAPI** for documentation.

---

## 🚀 Tech Stack
- **Java 17+**
- **Spring Boot**
- **Spring Security with JWT**
- **Spring Data JPA + MySQL**
- **Lombok** (reduce boilerplate code)
- **Validation API**
- **Springdoc OpenAPI (Swagger UI)**

---

## ✨ Features
- User Registration & Authentication (JWT-based)
- Role-Based Access Control (`USER`, `ADMIN`)
- CRUD APIs for:
  - Posts
  - Categories
  - Comments
- Pagination & Sorting for posts
- API Documentation with Swagger UI
- Input validation

---

## 📌 API Endpoints

### 🔐 Authentication
| Method | Endpoint              | Description                  |
|--------|------------------------|------------------------------|
| POST   | `/api/auth/register`   | Register new user            |
| POST   | `/api/auth/signup`     | Alternative register endpoint|
| POST   | `/api/auth/login`      | User login (JWT)             |
| POST   | `/api/auth/signin`     | Alternative login endpoint   |

---

### 📰 Posts
| Method | Endpoint                   | Description            |
|--------|-----------------------------|------------------------|
| GET    | `/api/posts`                | Get all posts (with pagination & sorting) |
| GET    | `/api/posts/{id}`           | Get post by ID         |
| POST   | `/api/posts`                | Create new post        |
| PUT    | `/api/posts/{id}`           | Update post            |
| DELETE | `/api/posts/{id}`           | Delete post            |
| GET    | `/api/posts/category/{id}`  | Get posts by category  |

---

### 📂 Categories
| Method | Endpoint              | Description        |
|--------|------------------------|--------------------|
| GET    | `/api/categories`      | Get all categories |
| GET    | `/api/categories/{id}` | Get category by ID |
| POST   | `/api/categories`      | Create category    |
| PUT    | `/api/categories/{id}` | Update category    |
| DELETE | `/api/categories/{id}` | Delete category    |

---

### 💬 Comments
| Method | Endpoint                                  | Description        |
|--------|--------------------------------------------|--------------------|
| GET    | `/api/posts/{postId}/comments`            | Get all comments for a post |
| GET    | `/api/posts/{postId}/comments/{id}`       | Get single comment |
| POST   | `/api/posts/{postId}/comments`            | Add comment to post|
| PUT    | `/api/posts/{postId}/comments/{id}`       | Update comment     |
| DELETE | `/api/posts/{postId}/comments/{id}`       | Delete comment     |

---

## 📖 Swagger API Documentation
Once the application is running, explore the Swagger UI here:  
👉 [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

OpenAPI Spec:  
👉 [http://localhost:8080/v3/api-docs](http://localhost:8080/v3/api-docs)

---

## ⚙️ Getting Started

### Prerequisites
- Java 17+
- Maven 3+
- MySQL installed and running

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/vishnubansode/springboot-blog-api.git
   cd springboot-blog-api

2.Update application.properties

spring.datasource.url=jdbc:mysql://localhost:3306/blogdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update


3.Build and run the project

mvn spring-boot:run


4.Access the API

http://localhost:8080

👨‍💻 Developed by Vishnu Bansode
📧 bansodevishnu24@gmail.com
