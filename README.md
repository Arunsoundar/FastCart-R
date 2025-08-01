**# FastCart - Inventory Management System**

A Spring Boot project to manage Products, Vendors, and Employees with integrated role-based security using Spring Security and MySQL.

---

**## Tech Stack**

- Java 17 
- Spring Boot 3
- Spring Security
- Spring Data JPA
- IntelliJ IDE
- MySQL
- Postman (for API testing)
- Lombok
- Maven


---

**## Authentication & Authorization**

### User Roles:
- `ADMIN` – Can perform CRUD on all endpoints.
- `USER` – Can **only view products** (`GET`).

### 🧪 Sample Users (Already in MySQL DB):

| Username | Password | Role  |
|----------|----------|-------|
| admin    | admin    | ADMIN |
| user     | user  | USER  |

🧂 Passwords are encrypted using **BCrypt**.
eg: 
admin : $2a$10$xkbavx1BcaAbEZbvNqzcL.REm8SOtRLg0CmAH0/ze0JhutpS0pwSW

---

**##  Modules & Endpoints**

###  Product APIs

| Method | Endpoint           | Access   |
|--------|--------------------|----------|
| GET    | `/product`         | USER/ADMIN |
| POST   | `/product`         | ADMIN   |
| PUT    | `/product/{id}`    | ADMIN   |
| DELETE | `/product/{id}`    | ADMIN   |

**###  Vendor APIs**

| Method | Endpoint          | Access   |
|--------|-------------------|----------|
| GET    | `/vendor`         | ADMIN   |
| POST   | `/vendor`         | ADMIN   |
| PUT    | `/vendor/{id}`    | ADMIN   |
| DELETE | `/vendor/{id}`    | ADMIN   |

**### Employee APIs**

| Method | Endpoint          | Access   |
|--------|-------------------|----------|
| GET    | `/employee`       | ADMIN   |
| POST   | `/employee`       | ADMIN   |

---

**Steps to Replicate : **

1. Download the code from this Repo.
2. Make sure the above tech stack available in your local.
3. Add new DB  "Fastcart" in your SQL localhost
4. Run the spring application. Tabel will be generated.
5. Update the Employee table with Encrypted password generated from your local. Encrypted passwords can get from println. 
6. Now through Postman , you can update/add/delete/retrieve the fields. Must need to add the Basic Auth in the headers.
7. Admin can do perform (add, delete,retrieve and update) , whereas User perform only retrieve.

  ** Product table Json :**
eg : 
   {
  "name": "Iphone",
  "description": "Iphone 16 128GB",
  "quantity": 20,
  "price": 89999.99,
  "category": "Mobiles",
  "vendorId": 3
}

  ** Vendor Table Json format:**
  eg : 
  {
   "email":"apple@support.com",
    "name": "Apple",
  "number": "044 123 768"
}

**CRUD Operations SnapShot Reference : **

_**Post Operation : Product  **_
<img width="1336" height="1029" alt="image" src="https://github.com/user-attachments/assets/61205399-4da5-4714-8615-7f917dbc21d6" />

_**Get Operation : Product  **_
<img width="1415" height="948" alt="image" src="https://github.com/user-attachments/assets/116c824e-b629-47dd-ae62-b969585b7fb2" />

_**Get by ID Operation : Product  **_
<img width="1397" height="663" alt="image" src="https://github.com/user-attachments/assets/92ca891b-608c-455d-9064-e1436ac6808a" />

_**Delete Operation : Product  **_
<img width="1406" height="516" alt="image" src="https://github.com/user-attachments/assets/0d391f60-5837-4d96-9801-4f35d2eee5bd" />

_**Put Operation : Product  **_ (Quantity was changed to 50 for id 3)
<img width="1377" height="985" alt="image" src="https://github.com/user-attachments/assets/a968ccbf-51d6-40af-87a9-c70964ae5f59" />

_**MYSQL table for product : **_
<img width="1244" height="673" alt="image" src="https://github.com/user-attachments/assets/8c4b8960-2410-4c8f-bff4-e261fa7f6be2" />




