# Greeting App – Spring Boot REST API

## Overview

Greeting App is a simple **Spring Boot REST API application** that performs CRUD operations for greeting messages.

The application allows users to create, retrieve, update, and delete greeting messages stored in a **MySQL database**.
All APIs are tested using **Postman**.

---

## Technologies Used

* Java 17
* Spring Boot
* Spring Data JPA
* MySQL
* Maven
* Postman
* Git & GitFlow

---

## Project Structure

```
greetingapp
 ├── controller
 │     GreetingController.java
 │
 ├── service
 │     GreetingService.java
 │
 ├── repository
 │     GreetingRepository.java
 │
 ├── entity
 │     Greeting.java
 │
 ├── resources
 │     application.properties
 │
 └── GreetingappApplication.java
```

---

## API Endpoints

### Create Greeting

```
POST /greeting
```

Example Request Body

```
{
  "message": "Hello World"
}
```

Example Response

```
{
  "id": 1,
  "message": "Hello World"
}
```

---

### Get Greeting by ID

```
GET /greeting/{id}
```

Example

```
GET /greeting/1
```

Example Response

```
{
  "id": 1,
  "message": "Hello World"
}
```

---

### Get All Greetings

```
GET /greetings
```

Example Response

```
[
  {
    "id": 1,
    "message": "Hello Deeksha"
  },
  {
    "id": 2,
    "message": "Hello World"
  }
]
```

---

### Update Greeting

```
PUT /greeting/{id}
```

Example Request Body

```
{
  "message": "Hello Updated World"
}
```

Example Response

```
{
  "id": 2,
  "message": "Hello Updated World"
}
```

---

### Delete Greeting

```
DELETE /greeting/{id}
```

Example Response

```
Greeting deleted successfully
```

---

## Running the Application

1. Clone the repository

```
git clone https://github.com/YOUR_GITHUB_USERNAME/Greeting-app.git
```

2. Navigate to project directory

```
cd Greeting-app
```

3. Run the application

```
mvn spring-boot:run
```

The application will start at

```
http://localhost:8080
```

---

## Testing APIs

All APIs can be tested using **Postman**.

Example:

```
POST http://localhost:8080/greeting
```

