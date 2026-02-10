# Tenant-Aware SaaS Management System

A fully containerized, tenant-aware Software-as-a-Service (SaaS) platform that enables multiple organizations to operate independently within a single application while maintaining strict data separation, access control, and subscription-based limits.

---

## 🌐 Overview

This project demonstrates a real-world SaaS architecture where each organization (tenant) can:

* Onboard with its own workspace
* Manage users and roles
* Create and track work items
* Operate under a subscription plan with enforced limits

The system is designed to be production-oriented, scalable, and easy to deploy using Docker.

---

## ✨ Core Capabilities

* **Tenant Isolation**: Each organization’s data is logically separated using tenant identifiers and subdomains.
* **Access Control**: Secure authentication using JWT with role-based permissions.
* **User Roles**:

  * System Owner (Super Admin)
  * Organization Admin
  * Organization Member
* **Plan Enforcement**: Feature and usage limits based on subscription tiers.
* **Work Management**: Create initiatives (projects) and actionable items (tasks).
* **Activity Insights**: Dashboard with counts, summaries, and recent actions.
* **Responsive Interface**: Modern UI that works across desktop and mobile devices.
* **Containerized Setup**: One-command startup using Docker Compose.

---

## 🛠️ Technology Stack

### Server Side

* Node.js
* Express.js
* PostgreSQL

### Client Side

* React
* Vite

### Infrastructure

* Docker
* Docker Compose

---

## 📋 System Requirements

* Docker Desktop (required)
* Node.js v18 or higher (optional, for local development)

---

## 🚀 Running the Application (Docker)

Follow these steps to start the entire system:

1. **Clone the repository**
2. **Launch all services**

   ```bash
   docker-compose up -d --build
   ```

This command will automatically:

* Initialize the PostgreSQL database
* Start the backend API server
* Start the frontend web application
* Run database migrations and seed default data

---

## 🔗 Application Endpoints

* **Web App**: [http://localhost:3000](http://localhost:3000)
* **API Health Check**: [http://localhost:5000/api/health](http://localhost:5000/api/health)

---

## 🔐 Preloaded Accounts (for Testing)

### System Owner

* Email: `superadmin@system.com`
* Password: `Admin@123`

### Organization Admin

* Email: `admin@demo.com`
* Password: `Demo@123`
* Workspace: `demo`

### Organization Member

* Email: `user1@demo.com`
* Password: `User@123`
* Workspace: `demo`

---

## 📡 API Overview

The backend exposes a REST-based API covering:

* Authentication & authorization
* Tenant and user management
* Project and task operations
* Subscription and usage checks

Complete endpoint details are available in:

```
docs/API.md
```

---

## 📁 Repository Layout

```
backend/        # API server and business logic
frontend/       # Client-side React application
database/       # Database schema, migrations, and seed scripts
docs/           # Technical and API documentation
docker-compose.yml
submission.json
```

---

## 🧪 Evaluation Notes

* The application starts with a **single Docker command**
* Database setup is fully automated
* No manual configuration required after cloning
* Designed to reflect real SaaS multi-tenant patterns

---

## 📄 License

This project is intended for educational and evaluation purposes.
