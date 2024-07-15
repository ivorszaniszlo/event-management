# Laravel 10 Event Management REST API

## Table of contents
* [General info](#general-info)
* [Description](#description)
* [Technologies](#technologies)
* [Setup](#setup)
* [Usage](#usage)
* [Running Tests](#running-tests)
* [Contributing](#contributing)
* [Created](#created)

## General info

Event Management application built with Laravel 10, providing a RESTFul API to seed and manage events for [Master Laravel for Beginners & Intermediate 2024 Udemy Course](https://www.udemy.com/course/laravel-beginner-fundamentals/learn/lecture/38206874#learning-tools).

## Description

This is a RESTful API for managing events, built with Laravel 10. The project uses Sanctum for authentication, gates and policies for authorization, and integrates various technologies for a robust development environment.

## Technologies

+ Laravel 10 with Sanctum Authentication, Gates and Policies Authorization
+ PHP 8
+ MySQL
+ Docker
+ Adminer DB management
+ Postman
+ Mailpit

## Setup

Clone the repository:

```bash
git clone git@github.com:ivorszaniszlo/event-management
```

Navigate to the project directory:

```bash
cd event-management
```

Install dependencies:

```bash
composer install
npm install
```

Set up environment variables:

```bash
cp .env.example .env
php artisan key:generate
```

### Docker Setup

Build and run the Docker containers:

```bash
docker-compose up --build
```

Access the application at `http://localhost:8000`.

### Run database migrations

```bash
docker-compose exec app php artisan migrate
```

### Seed the database with initial data

```bash
docker-compose exec app php artisan db:seed
```

## Usage

### Accessing the API

The API can be accessed at `http://localhost:8000/api`.

### Adminer

Adminer for database management can be accessed at `http://localhost:8080`.

### Mailpit

Mailpit for email testing can be accessed at `http://localhost:8025`.

### Authentication

The API uses Laravel Sanctum for authentication. To authenticate, obtain an API token by hitting the login endpoint:

```http
POST /api/login
```

Include the token in the `Authorization` header of your requests:

```http
Authorization: Bearer {token}
```

### Authorization

Gates and policies are used to authorize actions. Make sure to define your gates and policies in the appropriate places in your application.

### API Documentation

You can use Postman to test the API endpoints. Import the provided Postman collection to get started quickly. The collection file is located in the root directory of the project.

## Running Tests

You can use Postman to test the API endpoints. The Postman collection is located in the /tests/Postman/ directory. Import this collection into Postman to run the tests.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas.

## Created

2024
