
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

