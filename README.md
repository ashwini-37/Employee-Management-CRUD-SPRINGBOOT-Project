Overview
The Employee Management System (EMS) is a Spring Boot-based web application that allows users to perform CRUD (Create, Read, Update, Delete) operations on employee records. It provides an easy-to-use RESTful API for managing employee data, stored in an in-memory H2 database for testing and development purposes.

Features
Add Employee: Allows the creation of new employee records.
View Employees: Retrieves and displays employee records.
Update Employee: Updates details of an existing employee.
Delete Employee: Deletes an employee record from the system.
Employee List: Displays all employee records.
Technologies Used
Spring Boot: For building the backend application and RESTful APIs.
Spring Data JPA: For database interaction and object-relational mapping.
H2 Database: In-memory database for quick testing and development.
Maven: For project dependency management and build.
REST APIs: For exposing CRUD functionalities.
Prerequisites
Java 11 or higher.
Maven.
IDE (like IntelliJ IDEA, Eclipse) or a text editor.
Postman or any other tool for testing APIs.
Installation & Setup
Step 1: Clone the repository
bash
Copy code
git clone https://github.com/your-username/employee-management-springboot.git
Step 2: Navigate to the project directory
bash
Copy code
cd employee-management-springboot
Step 3: Build the project using Maven
bash
Copy code
mvn clean install
Step 4: Run the application
You can run the Spring Boot application using the command below:

bash
Copy code
mvn spring-boot:run
Alternatively, run the main class from your IDE.

API Endpoints
1. Add New Employee
Endpoint: POST /api/employees
Request Body:
json
Copy code
{
  "name": "John Doe",
  "designation": "Software Engineer",
  "department": "IT",
  "salary": 50000
}
Response:
json
Copy code
{
  "id": 1,
  "name": "John Doe",
  "designation": "Software Engineer",
  "department": "IT",
  "salary": 50000
}
2. Get Employee by ID
Endpoint: GET /api/employees/{id}
Response:
json
Copy code
{
  "id": 1,
  "name": "John Doe",
  "designation": "Software Engineer",
  "department": "IT",
  "salary": 50000
}
3. Get All Employees
Endpoint: GET /api/employees
Response:
json
Copy code
[
  {
    "id": 1,
    "name": "John Doe",
    "designation": "Software Engineer",
    "department": "IT",
    "salary": 50000
  },
  {
    "id": 2,
    "name": "Jane Smith",
    "designation": "HR Manager",
    "department": "HR",
    "salary": 60000
  }
]
4. Update Employee
Endpoint: PUT /api/employees/{id}
Request Body:
json
Copy code
{
  "name": "John Doe",
  "designation": "Senior Software Engineer",
  "department": "IT",
  "salary": 70000
}
Response:
json
Copy code
{
  "id": 1,
  "name": "John Doe",
  "designation": "Senior Software Engineer",
  "department": "IT",
  "salary": 70000
}
5. Delete Employee
Endpoint: DELETE /api/employees/{id}
Response:
json
Copy code
{
  "message": "Employee deleted successfully."
}
Database
H2 Database: The application uses H2 as an in-memory database, which automatically stores and manages employee data.
To view the H2 database console, access http://localhost:8080/h2-console/.
Testing APIs with Postman
Once the application is up and running, use Postman to test the APIs by sending HTTP requests to the endpoints listed above.
