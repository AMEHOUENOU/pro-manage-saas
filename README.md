## ProManage – Technical Specifications

### SaaS Appointment & Invoicing Management Platform

---

### 1. Project Overview

**1.1 Project Name**

* **ProManage** (Subject to change)

**1.2 Objective**
Develop a professional SaaS application designed for freelancers and SMEs to:

* Manage client databases
* Schedule and track appointments
* Automatically generate PDF invoices
* Monitor business performance via an analytics dashboard

**1.3 Key Goals**

* Build a high-quality portfolio showcase
* Create a reusable and customizable SaaS boilerplate
* Ensure production-ready deployment and scalability

---

### 2. User Roles

* **Administrator (Account Owner):** Full access to company settings, user management, and global financial statistics.
* **User (Employee/Staff):** Access to assigned client lists, personal appointment scheduling, and invoice generation.

---

### 3. Functional Requirements

**3.1 Authentication & Security**

* Secure Registration & Login
* JWT (JSON Web Tokens) for session management
* Bcrypt password hashing
* Role-Based Access Control (RBAC): ADMIN / USER

**3.2 Client Management**

* Full CRUD (Create, Read, Update, Delete) functionality
* Data fields: Name, Email, Phone, Address, and Client History

**3.3 Appointment Scheduling**

* Calendar-based management
* Status tracking: Scheduled, Completed, Canceled
* Linkage between clients, dates, and specific service descriptions

**3.4 Invoicing System**

* Automated PDF generation
* Unique sequential invoice numbering
* Direct linkage between an appointment and its invoice
* Downloadable PDF storage

**3.5 Dashboard & Analytics**

* Key Performance Indicators (KPIs): Total clients, Appointment volume, and Revenue
* Simple data visualization (charts and graphs)

**3.6 Mobile Application (MVP)**

* Secure Login
* Daily appointment agenda view
* Status update capabilities (e.g., marking a meeting as "Completed")

---

### 4. Technical Stack

| Layer | Technology |
| --- | --- |
| **Web Frontend** | Next.js 14 (App Router), TypeScript, Tailwind CSS |
| **Backend API** | Node.js, NestJS |
| **Database** | PostgreSQL with Prisma ORM |
| **Mobile App** | React Native (Expo) |
| **DevOps** | Docker, Docker Compose, GitHub Actions (CI/CD) |
| **Cloud Hosting** | Vercel (Frontend), Supabase/AWS (Database/Backend) |

---

### 5. Development Roadmap (15-Day Sprint)

* **Day 1:** Functional analysis, Tech setup, and Project initialization (Monorepo structure).
* **Days 2-3:** Backend Core: Database schema, NestJS modules, and Prisma integration.
* **Days 4-5:** Security Layer: JWT Auth implementation and User Role logic.
* **Days 6-7:** Business Logic: Client and Appointment CRUD APIs.
* **Days 8-9:** Invoicing: PDF generation engine and numbering logic.
* **Days 10-11:** Web UI: Dashboard layout, Auth forms, and Client/Appointment views.
* **Days 12-13:** Mobile & Integration: Expo setup and API consumption.
* **Days 14-15:** DevOps: Dockerization, CI/CD pipeline, and Production deployment.

---

### 6. System Architecture & Database

**Project Structure:**

```text
pro-manage-saas/
├── backend/       # NestJS, Prisma, Dockerfile
├── frontend/      # Next.js, Tailwind, Dockerfile
├── mobile/        # React Native (Expo)
├── .github/       # Workflows for CI/CD
└── docker-compose.yml

```

**Core Data Models:**

* **User:** `id, email, password, role, createdAt`
* **Client:** `id, name, email, phone, address, userId`
* **Appointment:** `id, date, status, clientId, userId`
* **Invoice:** `id, invoiceNumber, amount, appointmentId, createdAt`

---

### 7. Documentation (README.md)

**Description:** ProManage is a full-stack SaaS solution for small businesses.
**Core Features:** JWT Security, Client CRM, Automated Invoicing, Analytics Dashboard.
**Quick Start:**

1. Clone the repository.
2. Set up environment variables (`.env`).
3. Run `docker-compose up --build`.
