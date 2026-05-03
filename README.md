# CollegePrint: Industrial-Grade Printing Service 🚀

A high-performance document printing ecosystem designed for modern university campus environments. Featuring real-time infrastructure monitoring, advanced queue management, and a premium student experience.

## ✨ Core Features

### 👨‍🎓 Student Command Center
- **Premium UI/UX**: Modern Glassmorphism design with real-time status updates via WebSockets.
- **Smart Uploads**: Intelligent page counting for PDF/Office docs with automated cost engines (INR).
- **Quota Protection**: Integrated student daily limits (Print Quotas) to ensure fair resource allocation.
- **Live Tracking**: FCFS (First-Come-First-Served) queue position tracking with unique token assignment.
- **Secure Payments**: UPI-integrated payment proof verification system.

### 🛡️ Admin Infrastructure
- **Real-Time Monitoring**: Live dashboard for tracking hardware activity and queue health.
- **Audit Logs**: Comprehensive verification queue for payment audits.
- **Queue Control**: Start, pause, or complete physical printing jobs with hardware-ready status hooks.
- **Scalable Architecture**: Built for 10k+ concurrent requests using Spring Security 6 and JPA.

## 🛠️ Technology Stack
- **Backend**: Java 17, Spring Boot 3.2.5, Spring Security 6
- **Frontend**: Thymeleaf, Tailwind CSS 3.x, Alpine.js, Flowbite, Chart.js
- **Database**: MySQL 8.0, Redis (Session Management)
- **Communications**: Spring Messaging (STOMP over WebSockets)
- **Document Processing**: Apache PDFBox, Apache POI, Apache Tika

## 🏁 Setup Instructions

### 1. Prerequisites
- **OpenJDK 17+**
- **Maven 3.8+**
- **MySQL 8.0**
- **Redis Server** (optional for local dev, uses in-memory defaults)

### 2. Database Initialization
```sql
CREATE DATABASE document_printing_db;
CREATE USER 'printing_user'@'localhost' IDENTIFIED BY 'password123';
GRANT ALL PRIVILEGES ON document_printing_db.* TO 'printing_user'@'localhost';
```

### 3. Application Launch
```bash
mvn spring-boot:run
```
- **Student Access**: `http://localhost:8080/`
- **Admin Access**: `http://localhost:8080/admin/dashboard`
- **Default Admin**: `admin@printing.edu` / `Admin@123`