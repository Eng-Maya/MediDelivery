# Medicine Delivery & Pharmacy Management System 💊🚚

A backend RESTful API built with **Laravel** for managing **medicine delivery**, **pharmacies**, and **drug warehouses**.  
The system connects pharmacies, warehouses, drivers, and users in one platform to ensure fast, secure, and organized medicine distribution.

---

## 📌 Description

This application is designed to manage the full lifecycle of **medicine supply and delivery**, starting from warehouses, passing through pharmacies, and ending with users.

It supports:
- Managing pharmacies and drug warehouses
- Supplying medicines from warehouses to pharmacies
- Delivering medicines to users through drivers
- Secure authentication and role-based access
- Complaints, subscriptions, billing, and ratings

The system is built as an **API-only backend** to be used with web or mobile applications.

---

## 👥 System Roles

### 🔐 Admin
- Login and authentication
- Manage pharmacies, warehouses, drivers, and users
- Accept or reject join requests
- Soft delete and restore accounts
- View and manage complaints
- Monitor payments and subscriptions
- Update pharmacy and warehouse profiles
- View accepted, rejected, and pending requests

---

### 💊 Pharmacy
- Request to join the system
- Login and manage profile
- Add, update, and delete medicines
- Search medicines
- Request medicines from warehouses
- Accept or reject user medicine requests
- Create bills for users
- Manage subscriptions and payments
- Submit complaints
- View all pharmacy-related requests

---

### 🏬 Warehouse
- Request to join the system
- Login and manage profile
- Add and manage medicine inventory
- Receive requests from pharmacies
- Accept or reject pharmacy requests
- Manage subscriptions
- Submit complaints

---

### 🚚 Driver
- Request to join the system
- Login after admin approval
- Participate in medicine delivery process

---

### 👤 User
- Register and login
- Request medicines from pharmacies
- Receive bills
- Rate pharmacies and drivers
- Logout securely

---

## 🔄 Application Workflow

1. Pharmacy / Warehouse / Driver submits a join request  
2. Admin reviews and approves or rejects requests  
3. Warehouses supply medicines to pharmacies  
4. Pharmacies manage medicine stock  
5. Users request medicines from pharmacies  
6. Drivers deliver medicines  
7. Payments, subscriptions, and complaints are managed  

---

## 🔐 Authentication & Security
- Token-based authentication using **Laravel Sanctum**
- Protected routes with middleware
- Role-based access control
- Secure login and logout

---
## Tech Stack
- **Backend:** Laravel PHP
- **Database:** MySQL
- **Authentication:** Sanctum API
- **Other:** RESTful APIs, Middleware for access control

## Installation

1. Clone the repository:

```bash
   git clone https://github.com/YourUsername/Pharmacy-Management.git
```
---
## Install dependencies:

```bash
composer install
```

---
## Run migrations and seeders:

```bash
php artisan migrate --seed

```
---
## Start the server:
```bash
php artisan serve
```
