# Student Management System (Spring Boot + MySQL)

# Overview
This is a Spring Boot REST API for managing student records. It provides CRUD operations (Create, Read, Update, Delete) using Spring Boot, MySQL, and JPA.

# Technologies Used
- Java 17  
- Spring Boot (Spring Web, Spring Data JPA)  
- MySQL (Database)  
- Maven (Dependency Management)  
- Lombok (Reduces boilerplate code)  

# Setup Instructions

# 1. Clone the Repository
git clone https://github.com/your-username/student-management-system.git
cd student-management-system

# 2. Configure MySQL
Create a MySQL database:
sql
CREATE DATABASE studentdb;
Update `src/main/resources/application.properties` with your MySQL credentials.

# 3. Run the Project
mvn spring-boot:run

The API will start at:  
 `http://localhost:8080/students`

# API Endpoints

# Add a Student (POST)
curl -X POST http://localhost:8080/students -H "Content-Type: application/json" -d "{\"name\":\"John Doe\", \"age\":20, \"email\":\"johndoe@email.com\"}"


# Get All Students (GET)
curl -X GET http://localhost:8080/students


# Get Student by ID (GET)
curl -X GET http://localhost:8080/students/1


# Update Student (PUT)
curl -X PUT http://localhost:8080/students/1 -H "Content-Type: application/json" -d "{\"name\":\"John Updated\", \"age\":22, \"email\":\"john.updated@email.com\"}"


# Delete Student (DELETE)
curl -X DELETE http://localhost:8080/students/1
