# 🔐 Full Stack Authentication App — React + Vite + Spring Boot

A modern full-stack authentication system built using **React (Vite)** and **Spring Boot**. The application supports secure user authentication using **JWT**, **Google OAuth2**, and **GitHub OAuth2**, providing a scalable foundation for modern web applications.

---

## 🚀 Features

- User Registration & Login
- JWT Authentication (Access & Refresh Tokens)
- Google OAuth2 Login
- GitHub OAuth2 Login
- Role-Based Authentication
- Secure REST APIs
- Spring Security Integration
- Swagger/OpenAPI Documentation
- Responsive React UI
- Docker Support

---

# 🛠️ Tech Stack

## 🖥️ Frontend

- React (Vite)
- TypeScript
- Tailwind CSS
- Axios
- React Router DOM
- ShadCN UI

## ⚙️ Backend

- Java 21
- Spring Boot 3.x
- Spring Security 6.x
- Spring Data JPA
- Hibernate
- MySQL
- JWT Authentication
- OAuth2 (Google & GitHub)
- Maven
- Lombok
- HikariCP
- Swagger (OpenAPI)

---

# 📸 Screenshots

### Home Page

![Homepage](./screenshots/sc1.png)

### Login Page

![Login](./screenshots/sc2.png)

### Login Validation

![Login Error](./screenshots/sc3.png)

### Register Page

![Register](./screenshots/sc4.png)

### Dashboard

![Dashboard](./screenshots/sc5.png)

---

# 📁 Project Structure

```text
auth-app-boot-react/
│
├── auth-backend/
│   ├── src/
│   ├── pom.xml
│   ├── Dockerfile
│   └── application.yml
│
├── auth-front/
│   ├── src/
│   ├── package.json
│   ├── vite.config.ts
│   └── Dockerfile
│
├── screenshots/
└── README.md
```

---

# ⚙️ Backend Setup

## Prerequisites

- Java 21
- Maven 3.9+
- MySQL
- Git

## Clone Repository

```bash
git clone https://github.com/vivek5255-cell/auth-app-boot-react.git
cd auth-app-boot-react
```

## Create Database

```sql
CREATE DATABASE auth_app;
```

## Configure Database

Update

```
auth-backend/src/main/resources/application.yml
```

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/auth_app
    username: your_username
    password: your_password
```

## Configure Environment Variables

```text
JWT_SECRET=your-secret-key

GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret

GITHUB_CLIENT_ID=your-github-client-id
GITHUB_CLIENT_SECRET=your-github-client-secret
```

## Run Backend

```bash
cd auth-backend

mvn clean install

mvn spring-boot:run
```

Backend runs at

```
http://localhost:8083
```

Swagger UI

```
http://localhost:8083/swagger-ui/index.html
```

---

# 💻 Frontend Setup

```bash
cd auth-front

npm install
```

Create

```
.env
```

```env
VITE_BACKEND_URL=http://localhost:8083
```

Run

```bash
npm run dev
```

Frontend

```
http://localhost:5173
```

---

# 🔐 Authentication Flow

### Email & Password Authentication

```
User
   │
   ▼
React Frontend
   │
   ▼
Spring Boot REST API
   │
   ▼
Spring Security
   │
   ▼
JWT Generated
   │
   ▼
Authenticated User
```

---

### OAuth2 Authentication

```
React Application

↓

Google / GitHub

↓

Spring Security OAuth2

↓

JWT Generated

↓

Dashboard
```

---

# 📌 REST API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/auth/register` | Register User |
| POST | `/api/auth/login` | User Login |
| GET | `/api/auth/me` | Get Logged-in User |
| POST | `/api/auth/refresh` | Refresh JWT Token |
| POST | `/api/auth/logout` | Logout |
| GET | `/oauth2/authorization/google` | Google Login |
| GET | `/oauth2/authorization/github` | GitHub Login |

---

# 🐳 Docker

Build Docker Image

```bash
docker build -t auth-backend .
```

Run Container

```bash
docker run -p 8083:8083 auth-backend
```

---

# 📦 Common Commands

| Task | Command |
|------|---------|
| Run Backend | `mvn spring-boot:run` |
| Run Frontend | `npm run dev` |
| Package Backend | `mvn clean package` |
| Build Frontend | `npm run build` |
| Run JAR | `java -jar target/auth-app.jar` |

---

# 🚀 Deployment

Frontend

- Netlify
- Vercel

Backend

- Render
- Railway
- AWS EC2
- DigitalOcean

Remember to update

```
VITE_BACKEND_URL
```

with your production backend URL.

---

# 🌱 Future Improvements

- Email Verification
- Forgot Password
- Password Reset
- Two-Factor Authentication (2FA)
- Redis Token Storage
- Docker Compose
- CI/CD Pipeline
- Kubernetes Deployment

---

# 👨‍💻 Author

## Vivek Kumavat

**Java Full Stack Developer**

- 🎓 M.Sc. Computer Science
- 💻 Java | Spring Boot | React.js | MySQL
- 🌐 GitHub: https://github.com/vivek5255-cell
- 💼 LinkedIn: https://www.linkedin.com/in/vivek-kumavat/

---

# 🙏 Acknowledgements

This project was developed as part of my learning journey in Java Full Stack Development. I would like to acknowledge the educational resources that helped me understand Spring Boot, Spring Security, JWT Authentication, and OAuth2 concepts.

---

