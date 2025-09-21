The Library Management System is a comprehensive web application developed using Spring Boot and Thymeleaf to manage library operations.
The system is organized into several controllers following the MVC pattern, each responsible for distinct functionalities.

Library Management System
A full-featured web application for managing library operations, developed with Spring Boot and Thymeleaf. The system provides efficient management of books, members, and borrowing transactions through intuitive web interfaces and robust backend services.

Features
Manage book records: list, add, and update books
Manage library members: list, register, and update member information
Handle book borrowing and returns with real-time status
User-friendly web UI rendered with Thymeleaf templates
Uses Spring Data JPA for database operations and transactions
Clear separation of concerns with MVC architecture


Technologies Used:-
Java 17
Spring Boot (Web, Data JPA)
Thymeleaf Template Engine
MySQL or compatible relational database
Maven for dependency management

Project Structure
Controllers
BookController: Handles book catalog management (list, add).
MemberController: Manages library members (list, register, update).
BorrowingController: Controls borrowing and return workflows, connecting books and members.

Controllers in brief:-
BookController handles the management of book records. It supports listing all books, showing forms for adding new books, and saving book details to the database. This controller serves as the interface for librarians to maintain the book inventory efficiently.
BorrowingController manages the borrowing lifecycle of books. It facilitates displaying available books and members for borrowing, processing book lending, and handling returns. The controller interacts with the service layer to enforce business rules such as availability checks and transaction logging, ensuring a smooth borrowing workflow.
MemberController oversees member management. It provides endpoints to list registered members, display forms for member registration, update member information, and persist changes. This helps in maintaining an up-to-date roster of library users.

Getting Started

Prerequisites:-
Java Development Kit 17 or higher
Maven build tool
MySQL database setup with schema configured

Installation
Clone the repository:

Clone The Repository:-
git clone <repository-url>
cd library-management-system
Configure database connection in src/main/resources/application.properties:

Configure Database Connection in:-
spring.datasource.url=jdbc:mysql://localhost:3306/library_db
spring.datasource.username=your_db_username
spring.datasource.password=your_db_password
spring.jpa.hibernate.ddl-auto=update
Build and run the project:

Build And Run The Project:-
mvn clean install
mvn spring-boot:run
Open your browser at http://localhost:8080 to access the app.

Usage
Navigate to / to view the list of books
Add new books via /book/new
Manage members via /members and /member/new
Borrow books through the /borrow form
Return books through the /return form

Contributing
Contributions, issues, and feature requests are welcome. Fork the repository and create a pull request with detailed descriptions.

License
This project is licensed under the MIT License.
