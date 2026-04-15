# IS601 Module 10 – FastAPI Calculator with Secure User Model, Testing, and CI/CD

## 📌 Project Overview

This project extends a FastAPI-based calculator application by implementing a **secure user model**, **database integration**, **testing strategy**, and **CI/CD pipeline**.

The application uses SQLAlchemy for ORM, PostgreSQL as the database, Pydantic for validation, and Docker for containerization. GitHub Actions is used to automate testing and deployment to Docker Hub.

This project serves as a foundation for future modules and the final project.

---

## ⚙️ Features

* FastAPI calculator API
* Secure SQLAlchemy User model
* Password hashing and verification
* Pydantic schema validation
* PostgreSQL database integration
* Unit, integration, and end-to-end tests
* Dockerized application
* GitHub Actions CI/CD pipeline
* Docker Hub image deployment

---

## 🧠 Secure User Model

The User model includes:

* `username` (unique)
* `email` (unique)
* `password_hash` (secure storage)
* `created_at` timestamp

### 🔐 Password Security

* Passwords are hashed using bcrypt
* Plain-text passwords are never stored
* Verification function checks password correctness

---

## 📦 Project Structure

```bash
.
├── app/
│   ├── auth/
│   ├── models/
│   │   └── user.py
│   ├── schemas/
│   ├── database.py
│   ├── database_init.py
│   └── operations/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## 🧪 Testing

### Test Types

* **Unit Tests**

  * Password hashing
  * Schema validation
* **Integration Tests**

  * Database operations
  * Unique constraints (username/email)
* **End-to-End Tests**

  * API functionality

### 📊 Coverage

```
Total Coverage: 95%
57 Passed | 1 Skipped | 1 Pending Fix
```

---

## 🐳 Running the Project Locally

### Step 1: Clone Repo

```bash
git clone https://github.com/kdulobo12/IS601_Module10
cd IS601_Module10
```

---

### Step 2: Setup Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

### Step 3: Run with Docker

```bash
docker compose down -v
docker compose up --build
```

---

### Step 4: Access Application

* FastAPI App → http://localhost:8000
* Swagger Docs → http://localhost:8000/docs
* pgAdmin → http://localhost:5050

---

## 🧪 Run Tests

```bash
pytest
```

With coverage:

```bash
pytest --cov=app --cov-report=html
```

Open:

```bash
htmlcov/index.html
```

---

## 🔄 CI/CD Pipeline

GitHub Actions workflow performs:

1. Install dependencies
2. Run all tests
3. Build Docker image
4. Push image to Docker Hub

---

## 🐳 Docker Hub Repository

👉 **Docker Image Link:**
https://hub.docker.com/r/kdulobo12/module10-fastapi

---

## 📸 Screenshots (Add Here)

### ✅ GitHub Actions Success

(Add screenshot here)

### ✅ Docker Hub Image

(Add screenshot here)

---



## 📋 Submission Checklist

* [x] SQLAlchemy User Model
* [x] Pydantic Schemas
* [x] Password Hashing
* [x] Unit Tests
* [x] Integration Tests
* [x] Docker Setup
* [x] GitHub Actions
* [x] Docker Hub Deployment
* [x] README Documentation
* [x] Reflection

---

## 👩‍💻 Author

Krupa Adulobo
GitHub: https://github.com/kdulobo12
