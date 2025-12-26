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

### 🏬 Warehouse
- Request to join the system
- Login and manage profile
- Add and manage medicine inventory
- Receive requests from pharmacies
- Accept or reject pharmacy requests
- Manage subscriptions
- Submit complaints

### 🚚 Driver
- Request to join the system
- Login after admin approval
- Participate in medicine delivery process

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

## ⚡ API Endpoints

### 🔐 Admin Routes
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/admin/login` | Admin login |
| GET    | `/admin/pharmacies` | List all pharmacies |
| POST   | `/admin/approve_pharmacy/{id}` | Approve a pharmacy request |
| POST   | `/admin/reject_pharmacy/{id}` | Reject a pharmacy request |
| GET    | `/admin/warehouses` | List all warehouses |
| POST   | `/admin/approve_warehouse/{id}` | Approve warehouse request |
| POST   | `/admin/reject_warehouse/{id}` | Reject warehouse request |
| GET    | `/admin/drivers` | List all drivers |
| POST   | `/admin/approve_driver/{id}` | Approve driver request |
| POST   | `/admin/reject_driver/{id}` | Reject driver request |
| GET    | `/admin/users` | List all users |
| DELETE | `/admin/delete_user/{id}` | Soft delete user |
| PUT    | `/admin/restore_user/{id}` | Restore deleted user |
| GET    | `/admin/complaints` | List all complaints |
| GET    | `/admin/complaint/{id}` | View complaint details |
| PUT    | `/admin/update_profile/{id}` | Update admin profile |

---

### 💊 Pharmacy Routes
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/pharmacy/register` | Request to join as pharmacy |
| POST   | `/pharmacy/login` | Pharmacy login |
| GET    | `/pharmacy/medicines` | List all medicines |
| POST   | `/pharmacy/add_medicine` | Add a new medicine |
| PUT    | `/pharmacy/update_medicine/{id}` | Update medicine details |
| DELETE | `/pharmacy/delete_medicine/{id}` | Delete medicine |
| GET    | `/pharmacy/requests` | List all user medicine requests |
| POST   | `/pharmacy/accept_request/{id}` | Accept medicine request |
| POST   | `/pharmacy/reject_request/{id}` | Reject medicine request |
| POST   | `/pharmacy/create_bill/{userId}` | Create bill for user |
| GET    | `/pharmacy/subscriptions` | View subscriptions |
| POST   | `/pharmacy/complaints` | Submit complaint |

---

### 🏬 Warehouse Routes
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/warehouse/register` | Request to join as warehouse |
| POST   | `/warehouse/login` | Warehouse login |
| GET    | `/warehouse/medicines` | List all medicines in inventory |
| POST   | `/warehouse/add_medicine` | Add medicine to inventory |
| PUT    | `/warehouse/update_medicine/{id}` | Update medicine info |
| GET    | `/warehouse/requests` | View requests from pharmacies |
| POST   | `/warehouse/accept_request/{id}` | Accept pharmacy request |
| POST   | `/warehouse/reject_request/{id}` | Reject pharmacy request |
| GET    | `/warehouse/subscriptions` | View subscriptions |
| POST   | `/warehouse/complaints` | Submit complaint |

---

### 🚚 Driver Routes
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/driver/register` | Request to join as driver |
| POST   | `/driver/login` | Driver login |
| GET    | `/driver/deliveries` | View assigned deliveries |
| PUT    | `/driver/update_delivery/{id}` | Update delivery status |

---

### 👤 User Routes
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/user/register` | Register new user |
| POST   | `/user/login` | User login |
| GET    | `/user/medicines` | View available medicines from pharmacies |
| POST   | `/user/request_medicine/{pharmacyId}` | Request medicine from pharmacy |
| GET    | `/user/bills` | View user bills |
| POST   | `/user/complaints` | Submit complaint |
| POST   | `/user/logout` | Logout securely |

---

### 🛠 Tech Stack
- **Backend:** Laravel PHP  
- **Database:** MySQL  
- **Authentication:** Sanctum API  
- **Other:** RESTful APIs, Middleware for access control  

---

### 🖥 Installation

1. Clone the repository:

```bash
git clone https://github.com/YourUsername/Pharmacy-Management.git
