
## Project Overview

**Employee Tracker** is a Laravel-based web application designed to manage employees and departments efficiently. It demonstrates core Laravel features including:

* MVC architecture
* Blade templating
* Database migrations
* Eloquent ORM relationships
* Soft deletes
* Factories and seeders

Additionally, it offers a full RESTful API with token-based authentication (using Laravel Sanctum), enabling secure access to employee and department data.

---

## Features

* Laravel MVC with Blade templating for user-friendly UI
* Employee CRUD operations with search, filter, and pagination
* Soft delete & restore functionality for employee records
* Fully implemented database migrations & seeding with realistic fake data
* Model relationships: Employee-Department & Employee-EmployeeDetail
* RESTful API with full CRUD for employees and departments
* Token-based authentication with Laravel Sanctum
* API pagination, validation, and soft delete support
* Tested with Postman for consistent JSON responses

---

## Technology Stack

* Laravel (PHP framework)
* MySQL database
* Blade templating engine
* Laravel Sanctum for API authentication
* Faker for data factories
* XAMPP (Apache + MySQL) for local development
* Postman for API testing

---

## Installation & Setup

### Install dependencies

* Run the following command (only if `vendor/` folder does not exist):

  ```bash
  composer install
  ```

### Environment configuration

* Update your `.env` file with your database credentials:

  ```env
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=employee_tracker
  DB_USERNAME=root
  DB_PASSWORD=
  ```

### Generate application key

* Run:

  ```bash
  php artisan key:generate
  ```

### Create database

* Create a database named `employee_tracker` (using phpMyAdmin or MySQL CLI).

### Run migrations and seeders

* Run:

  ```bash
  php artisan migrate:fresh --seed
  ```

* This will:

  * Drop all existing tables
  * Recreate tables using migration files
  * Insert realistic fake data using factories & seeders

---

## Running the Application

* Start the development server:

  ```bash
  php artisan serve
  ```

* Visit the application in your browser at:
  `http://127.0.0.1:8000/employees`

---

## API Documentation

### Authentication

| Endpoint     | Method | Description                                     | Requires Auth? |
| ------------ | ------ | ----------------------------------------------- | -------------- |
| `/api/login` | POST   | Login with email & password; returns auth token | No             |
| `/api/user`  | GET    | Get current authenticated user info             | Yes            |

---

### Departments

| Endpoint                | Method    | Description             | Auth Required |
| ----------------------- | --------- | ----------------------- | ------------- |
| `/api/departments`      | GET       | List all departments    | Yes           |
| `/api/departments`      | POST      | Create a new department | Yes           |
| `/api/departments/{id}` | GET       | Get a department by ID  | Yes           |
| `/api/departments/{id}` | PUT/PATCH | Update a department     | Yes           |
| `/api/departments/{id}` | DELETE    | Delete a department     | Yes           |

---

### Employees

| Endpoint                      | Method    | Description                     | Auth Required |
| ----------------------------- | --------- | ------------------------------- | ------------- |
| `/api/employees`              | GET       | List all employees (paginated)  | Yes           |
| `/api/employees`              | POST      | Create a new employee           | Yes           |
| `/api/employees/{id}`         | GET       | Get a single employee by UUID   | Yes           |
| `/api/employees/{id}`         | PUT/PATCH | Update an employee              | Yes           |
| `/api/employees/{id}`         | DELETE    | Soft delete an employee         | Yes           |
| `/api/employees/{id}/restore` | POST      | Restore a soft deleted employee | Yes           |

---
## 

<img width="933" height="532" alt="11" src="https://github.com/user-attachments/assets/e143f39b-56c2-4f3e-9c31-cf1c27507e3a" />
##
<img width="934" height="557" alt="11 1" src="https://github.com/user-attachments/assets/df863398-935b-4fb2-92e5-75ffbfe3cf13" />
##
<img width="943" height="622" alt="12" src="https://github.com/user-attachments/assets/c2ddefac-d8a5-4bdd-bf65-d842a5adf9c6" />
##
<img width="932" height="614" alt="13" src="https://github.com/user-attachments/assets/739cb250-e50c-431f-b592-73e7baa2160a" />
##
<img width="936" height="494" alt="14" src="https://github.com/user-attachments/assets/afae40ac-70b0-4194-aaae-709ce1c44f3a" />
##
<img width="935" height="636" alt="15" src="https://github.com/user-attachments/assets/9c3abab9-2881-45b8-b0f9-8976dfef2276" />
##
<img width="1361" height="354" alt="16" src="https://github.com/user-attachments/assets/09f4dab8-e411-4ae1-a755-1446a20b1e20" />
##
<img width="941" height="619" alt="17" src="https://github.com/user-attachments/assets/f76a76d4-2794-4956-983a-2b13f3f5c85e" />
##
<img width="943" height="632" alt="18" src="https://github.com/user-attachments/assets/8b001cd3-40e4-4cfe-897b-a6f16426d289" />
##
<img width="939" height="607" alt="19" src="https://github.com/user-attachments/assets/d7202227-75f9-449f-b065-58748c76a6f5" />
##
<img width="940" height="631" alt="20" src="https://github.com/user-attachments/assets/bf4b9da0-e707-40a9-bfe7-50b711b83d6e" />
##
<img width="940" height="427" alt="21" src="https://github.com/user-attachments/assets/e55ef070-d505-472d-9ab6-a3367cb2aa3f" />
##
<img width="942" height="580" alt="22" src="https://github.com/user-attachments/assets/45937526-ccef-4eb2-816d-72abfa1cd976" />

