# 🔐 Secure User Management API (Enterprise-Grade)

A production-ready **.NET Web API** demonstrating **security**, **reliability**, and **scalability** through a professionally designed User Management System.

This project is designed as a portfolio piece to showcase backend engineering skills, API clean architecture, database security, and Docker-based deployment.

---

# ⭐ Features

## 🔐 Security-Focused
- Password hashing (PBKDF2)
- AES encryption for sensitive fields
- JWT authentication with refresh token
- Role-based access control (Admin / User)
- SQL injection protection
- Login attempt limiter
- Centralized error handling middleware
- Secure input validation

## 🏗 Reliable & Maintainable
- Layered architecture (Controller → Service → Repository)
- Consistent response template
- Async logging with fire-and-forget
- Database transactions for critical operations
- PostgreSQL stored functions

## 📈 Scalable Architecture
- Stateless API (ready for horizontal scaling)
- Dockerized (.NET + PostgreSQL)
- Optimized queries & indexes
- Clean modular folder structure

---

# 📂 Project Structure
secure-user-management-api/
│
├── SecureUserManagement.Api/
│   ├── Controllers/
│   │   └── AuthController.cs
│   │   └── UsersController.cs
│   │
│   ├── Services/
│   │   └── AuthService.cs
│   │   └── UserService.cs
│   │
│   ├── Repositories/
│   │   └── UserRepository.cs
│   │
│   ├── Models/
│   │   ├── Entities/
│   │   │   └── User.cs
│   │   ├── DTOs/
│   │   │   └── RegisterRequest.cs
│   │   │   └── LoginRequest.cs
│   │   │   └── AuthResponse.cs
│   │
│   ├── Security/
│   │   ├── JwtTokenHelper.cs
│   │   ├── PasswordHasher.cs
│   │   ├── EncryptionHelper.cs
│   │
│   ├── Middleware/
│   │   └── ErrorHandlingMiddleware.cs
│   │   └── LoggingMiddleware.cs
│   │
│   ├── Database/
│   │   └── user_functions.sql
│   │
│   ├── Config/
│   │   └── JwtSettings.cs
│   │
│   ├── Program.cs
│   ├── appsettings.json
│   └── SecureUserManagement.Api.csproj
│
├── docker-compose.yml
├── README.md
└── .gitignore

# 🧩 Endpoints

### **Auth**
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login and get JWT token |
| POST | `/api/auth/refresh` | Get new access token |

### **User**
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/users/me` | Get own user profile |
| GET | `/api/users` | Admin-only: list all users |

---

# 🛠 Technology Stack

- **Backend:** .NET 8 Web API  
- **Database:** PostgreSQL  
- **Security:** JWT, PBKDF2, AES encryption  
- **ORM:** Dapper  
- **Containerization:** Docker & Docker Compose
