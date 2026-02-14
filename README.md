# Multi-Tenant SaaS Platform

A complete multi-tenant SaaS application with JWT authentication, RBAC, project/task management, subscription enforcement, audit logging, and one-command Docker startup.

---

## ✨ Features

- JWT-based authentication
- Role-Based Access Control (Super Admin, Tenant Admin, User)
- User management (CRUD)
- Project & Task management
- Subscription plan enforcement
- Audit logging
- Fully Dockerized (Database, Backend, Frontend)
- One-command startup using Docker Compose

---

## 🛠 Tech Stack

- **Backend:** Node.js, Express  
- **Frontend:** React  
- **Database:** PostgreSQL  
- **Authentication:** JWT  
- **Authorization:** RBAC  
- **Containerization:** Docker, Docker Compose  

---

## 📁 Project Structure

```bash
project-root/
├── backend/
├── frontend/
├── database/
│   └── init/
│       └── init.sql
├── docs/
│   ├── research.md
│   ├── PRD.md
│   ├── architecture.md
│   └── technical-spec.md
├── docker-compose.yml
└── README.md
🚀 Getting Started
Prerequisites
Docker Desktop (Linux containers enabled)

Git

Clone the Repository
bash
git clone https://github.com/JAHNAVISINDHU/multi-saas.git
cd multi-saas
🐳 Run with Docker (One Command)
From the project root:

bash
docker-compose down -v --remove-orphans
docker-compose up -d --build
All services (database, backend, frontend) start together.

Database schema and seed data are loaded automatically.

No manual setup required.

To stop all services:

bash
docker-compose down -v
🔎 Service URLs
Service	URL
Frontend	http://localhost:3000
Backend	http://localhost:5000
Health Check	http://localhost:5000/api/health
🔐 Authentication Flow
Register a tenant.

Log in to receive a JWT.

Use the token in the Authorization header for protected routes.

text
Authorization: Bearer <your-jwt-token>
Example (for reference only, do not hardcode in production):

text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI5ODQzMzEzZS00ZjU0LTRiZWEtYjA1Zi1iZTViNmRkNjhjMTQiLCJ0ZW5hbnRJZCI6IjUyYjlhMDQ5LTgyZjctNGE1OS05YjkwLWRkYWM2NjA0YWJhMCIsInJvbGUiOiJ0ZW5hbnRfYWRtaW4iLCJpYXQiOjE3NjYyOTk2NDgsImV4cCI6MTc2NjM4NjA0OH0.AtRK0Y5xCS68eKiEB0GCCFR57-Z5j6NSmcwFAaPr2VM
📊 Subscription Plans
Plan	Max Users	Max Projects
Free	5	3
Pro	25	15
Enterprise	100	50
Subscription limits are enforced at the application level based on the selected plan.

👥 Roles & Access
Super Admin

Global management of tenants and system-level configuration.

Tenant Admin

Manages users, projects, and tasks within their tenant.

User

Access to assigned projects and tasks within their tenant.

📄 Documentation
All detailed documentation is available in the docs/ folder:

research.md – Research & analysis

PRD.md – Product requirements

architecture.md – Architecture & ERD

technical-spec.md – Technical specification

📝 Notes for Evaluators
Entire system starts with one command using Docker Compose.

Database schema and seed data are applied automatically.

No manual database or environment setup is required for basic usage.

📎 Repository
GitHub: https://github.com/JAHNAVISINDHU/multi-saas