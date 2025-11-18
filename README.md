Demo Spring Boot Student API


How to run
----------
1. Open the project in your IDE (for example IntelliJ).
2. Run the main class: com.example.demo.DemoApplication

Alternatively, from the project folder in a terminal:
- On macOS / Linux: ./mvnw spring-boot:run
- On Windows: mvnw.cmd spring-boot:run

The application runs on: http://localhost:8080

REST endpoints
--------------
Base path: /students

1) Get all students
   GET http://localhost:8080/students

2) Get a student by id
   GET http://localhost:8080/students/{id}
   Example: http://localhost:8080/students/1

3) Create a new student
   POST http://localhost:8080/students
   Content-Type: application/json
   Body example:
   {
     "name": "Alice",
     "age": 20
   }

4) Update a student
   PUT http://localhost:8080/students/{id}
   Content-Type: application/json
   Body example:
   {
     "name": "Alice Updated",
     "age": 21
   }

5) Delete a student
   DELETE http://localhost:8080/students/{id}

H2 database console
-------------------
You can view the data using the H2 web console.

URL:
http://localhost:8080/h2-console

Use these settings:
JDBC URL: jdbc:h2:mem:testdb
User: sa
Password: (leave empty)

Example query after you have created some students:
SELECT * FROM STUDENT;

Note: The H2 database is in-memory. All data is lost when you stop the application.

Swagger UI
----------

This project includes Swagger UI for viewing and testing the REST API.

After starting the application, open:

http://localhost:8080/swagger-ui.html

From there you can:
- See all available endpoints (e.g. /students)
- Try GET / POST / PUT / DELETE requests directly from the browser