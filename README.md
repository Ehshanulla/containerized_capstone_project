# Investment Banking Deal Pipeline Management System

## 📌 Project Overview

The **Investment Banking Deal Pipeline Management System** is a full-stack web application designed to help investment banks manage, track, and monitor deals throughout their lifecycle. It digitizes real-world investment banking workflows and provides secure, role-based access to deal data.

This project is built as a **capstone-level enterprise application** using modern technologies and best practices.

---

## 🏗️ Tech Stack

### Reverse Proxy

* **Nginx** (used as a reverse proxy between frontend and backend)

### Frontend

* Angular
* Bootstrap

### Backend

* Java
* Spring Boot
* Spring Security
* JWT Authentication

### Database

* MongoDB

### DevOps & Quality

* Docker & Docker Compose
* SonarQube

---

## 🎯 Features

* User authentication & authorization (JWT)
* Role-based access control (Admin, Banker, Viewer)
* Deal creation, update, deletion
* Deal pipeline stage tracking
* Kanban-style deal visualization
* Search & filtering
* Secure REST APIs
* Containerized deployment

---

## 🔐 User Roles

### Admin

* Manage users and roles
* View all deals
* Monitor system activity

### Banker / Analyst

* Create and manage deals
* Move deals across pipeline stages
* View assigned deals

### Viewer

* Read-only access to deals

---

## 🔄 Deal Pipeline Stages

1. Origination
2. Initial Review
3. Due Diligence
4. Negotiation
5. Approval
6. Closure
7. Archived / Failed

---

## 🌐 Nginx Reverse Proxy Configuration

Nginx is used as a **reverse proxy** to route requests between the frontend and backend, providing:

* A single entry point for the application
* Better security (backend not directly exposed)
* Simplified CORS handling
* Production-like deployment setup

### Request Flow

```
Browser → Nginx → Angular Frontend
                → Spring Boot Backend (API)
```

### Example Routing Logic

* `/` → Angular Frontend
* `/api/*` → Spring Boot Backend

---

## 🚀 Running the Project (Docker)

```bash
# Build and start all services
docker-compose up -d
```

Access:

* Frontend: `http://localhost:4200`
* Backend API: `http://localhost:8080`

---

## 📡 API Documentation

### 🔑 Authentication APIs

| Method | Endpoint       | Description                    |
| ------ | -------------- | ------------------------------ |
| POST   | /auth/login    | User login                     |
| POST   | /auth/refresh  | Refresh JWT token              |
| POST   | /auth/register | Register new user (Admin only) |

---

### 👤 User APIs

| Method | Endpoint         | Description           |
| ------ | ---------------- | --------------------- |
| GET    | /users           | Get all users (Admin) |
| PUT    | /users/{id}/role | Update user role      |
| DELETE | /users/{id}      | Delete user           |

---

### 💼 Deal APIs

| Method | Endpoint          | Description       |
| ------ | ----------------- | ----------------- |
| GET    | /deals            | Get all deals     |
| GET    | /deals/{id}       | Get deal by ID    |
| POST   | /deals            | Create new deal   |
| PUT    | /deals/{id}       | Update deal       |
| PATCH  | /deals/{id}/stage | Update deal stage |
| DELETE | /deals/{id}       | Delete deal       |

---

## 🗄️ Database Schema (MongoDB)

### 🧑 Users Collection

```
Users
-----
_id: ObjectId
username: String
email: String
password: String (hashed)
role: String (ADMIN | BANKER | VIEWER)
createdAt: Date
```

---

### 💼 Deals Collection

```
Deals
-----
_id: ObjectId
title: String
clientName: String
dealValue: Number
stage: String
assignedBankerId: ObjectId
status: String
createdAt: Date
updatedAt: Date
```

---

### 🔗 Relationship Diagram

```
Users (1) ──────< (Many) Deals
```

---

## 🧪 Testing & Code Quality

* Backend unit tests
* Angular component tests
* SonarQube for static code analysis

---

## 🔒 Security

* JWT access & refresh tokens
* Password hashing
* CORS configuration
* Role-based endpoint protection

---

## 📦 Deployment

* Fully containerized using Docker
* Environment-based configuration
* Easily deployable on cloud platforms

---

## 🚧 Future Enhancements

* Email notifications
* Advanced analytics dashboard
* AI-based deal risk scoring
* Blockchain-based audit trail

---

## 📄 License

This project is for academic and learning purposes.

---

## 🙌 Author

**Tappal Ehshanulla**
Capstone Project
