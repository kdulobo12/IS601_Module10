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

<img width="3340" height="1476" alt="image" src="https://github.com/user-attachments/assets/a44bce55-f3ff-4537-8aa0-6ebbf9403bad" />


### ✅ Docker Hub Image

<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/eea8668c-bcc7-4a80-8e7d-9f9399a9dbc8" />

Link: https://hub.docker.com/r/kdulobo12/module10-fastapi
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


## Reflection

This project helped me better understand how backend components work together in a real application. I practiced building a secure user model with SQLAlchemy, validating input and output with Pydantic, and hashing passwords before storing them in the database.
One of the biggest challenges was debugging Docker and PostgreSQL configuration issues. I ran into container name conflicts, database connection errors, and a PostgreSQL image/version mismatch related to Docker volumes. Working through those issues taught me how important container configuration, version pinning, and clean rebuilds are in real projects.
I also learned how to separate unit tests from integration tests and how to use coverage reports to identify missing execution paths. Setting up CI/CD with GitHub Actions and Docker Hub gave me a better understanding of how automated testing and deployment work in practice.
Overall, this project gave me hands-on experience with secure backend development, testing, containers, and deployment automation, and it created a strong base for the future modules and final project.

---

## 👩‍💻 Author

Krupa Adulobo
GitHub: https://github.com/kdulobo12
