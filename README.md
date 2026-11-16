<div align="center">

# ⚡ NextGen CRM & Lead Management System

**High-performance Asynchronous CRM & Scraping Engine built with FastAPI, PostgreSQL & Playwright**

[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-asyncpg-336791?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0_Async-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)](https://www.sqlalchemy.org/)

</div>

---

## 📌 Overview

**NextGen CRM** is an enterprise-grade backend system designed for client management, automated lead scraping, deal pipelines, and administrative workflows. Built on top of **FastAPI** with 100% asynchronous I/O (`asyncio`, `asyncpg`), it provides lightning-fast response times and handles concurrent automated background tasks seamlessly.

---

## 🚀 Key Features

- **⚡ Asynchronous Architecture**: Non-blocking database transactions powered by `SQLAlchemy 2.0 (AsyncIO)` and `asyncpg`.
- **🔐 Secure Authentication**: JWT (JSON Web Tokens) with role-based access control (RBAC) and bcrypt password hashing.
- **🕷️ Headless Automation & Web Scraping**: Integrated `Playwright` and `BeautifulSoup4` for lead data extraction and verification.
- **📊 SQLAdmin Dashboard**: Rich web-based administrative panel (`sqladmin`) for real-time model management.
- **🔄 Database Migrations**: Automated schema tracking and rollbacks using `Alembic`.
- **🐳 Dockerized Deployment**: Multi-container setup with `docker-compose` for rapid production deployment.
- **🧪 Comprehensive Test Suite**: Asynchronous unit and integration tests using `pytest` and `pytest-asyncio`.

---

## 🛠 Tech Stack

| Layer | Technologies |
| :--- | :--- |
| **Backend Framework** | [FastAPI](https://fastapi.tiangolo.com/), Uvicorn |
| **Database & ORM** | PostgreSQL, [SQLAlchemy 2.0 (Async)](https://docs.sqlalchemy.org/), [Alembic](https://alembic.sqlalchemy.org/) |
| **Database Driver** | `asyncpg` (ultra-fast asynchronous PostgreSQL client) |
| **Data Validation** | [Pydantic v2](https://docs.pydantic.dev/) & `pydantic-settings` |
| **Automation & Scraping** | [Playwright](https://playwright.dev/python/), BeautifulSoup4, `lxml` |
| **Admin Panel** | [SQLAdmin](https://aminalaee.dev/sqladmin/) |
| **Security & Auth** | PyJWT, Passlib / Bcrypt |
| **DevOps & Testing** | Docker, Docker Compose, Pytest, Pytest-AsyncIO |

---

## 📁 Project Architecture

```
CRM/
├── backend/
│   ├── app/
│   │   ├── api/            # API endpoints & routes (v1)
│   │   ├── core/           # Config, security, database engine
│   │   ├── models/         # SQLAlchemy 2.0 async models
│   │   ├── schemas/        # Pydantic v2 schemas
│   │   ├── services/       # Business logic & Playwright scrapers
│   │   └── admin/          # SQLAdmin views
│   ├── alembic/            # Database migration scripts
│   ├── tests/              # Pytest asynchronous tests
│   ├── requirements.txt    # Production dependencies
│   └── main.py             # Application entrypoint
├── frontend/               # Web client interface
├── deploy/                 # Production deployment manifests & configs
├── docker-compose.yml      # Multi-container orchestration
└── .env                    # Environment variables
```

---

## ⚙️ Quick Start (Docker)

The fastest way to spin up the entire CRM ecosystem with PostgreSQL:

```bash
# 1. Clone the repository
git clone https://github.com/sunnatila/CRM.git
cd CRM

# 2. Configure environment
cp .env.example .env

# 3. Build and run containers
docker-compose up -d --build

# 4. View API Documentation
# Interactive Swagger UI: http://localhost:8000/docs
# ReDoc: http://localhost:8000/redoc
# Admin Dashboard: http://localhost:8000/admin
```

---

## 💻 Local Development Setup

```bash
# Navigate to backend directory
cd backend

# Create and activate virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
alembic upgrade head

# Start development server
uvicorn main:app --reload --port 8000
```

---

## 🧪 Running Tests

```bash
pytest -v
```

---

## 👨‍💻 Author

**Sunnatilla Sharipov**
- GitHub: [@sunnatila](https://github.com/sunnatila)
- Telegram: [@sunnatillasharipov](https://t.me/sunnatillasharipov)
- Email: sunnatillasharipov6@gmail.com
