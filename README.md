﻿# Student Management System

## Overview
The Student Management System is a comprehensive application designed to manage various aspects of a school environment, including students, teachers, parents, classrooms, homework assignments, and more. The system is built using a robust and scalable technology stack, making it suitable for deployment in small to large-scale educational institutions.

## Features
- **Student Management**: Manage student profiles, including their addresses, reports, and associated parents.
- **Teacher Management**: Handle teacher profiles, subject assignments, and classrooms.
- **Parent Portal**: Parents can view their children's progress and reports.
- **Homework Tracking**: Teachers can assign homework to students and track submissions.
- **Classroom Management**: Manage classroom details and assign students and teachers.
- **School Administration**: Manage school information, including subjects and school-wide reports.
- **User Authentication**: Secure login and role-based access for administrators, teachers, students, and parents.

## Technology Stack

### Backend
- **Java**: The primary programming language for the application.
- **Spring Framework**: Used for dependency injection, aspect-oriented programming, and transaction management.
- **Spring Boot**: Facilitates rapid application development with Spring, offering embedded servers, auto-configuration, and more.

### Frontend
- **HTML/CSS**: Structure and styling of the web pages.
- **JavaScript**: Provides interactivity and dynamic content.
- **Thymeleaf**: Template engine for rendering server-side HTML content.

### Database
- **MySQL / PostgreSQL / AzureSQL**: For production-grade relational database management.
- **H2 Database**: For in-memory testing and development.
- **MongoDB**: For handling unstructured data.

## Entities

The system is designed with the following core entities:

- **Address**: Stores addresses of students, parents, teachers, etc.
- **Classroom**: Manages information related to classrooms and their assignments.
- **Homework**: Tracks homework assignments, submissions, and evaluations.
- **Parent**: Contains parent profiles linked to students.
- **Report**: Stores academic reports for students.
- **School**: Represents the overall school entity.
- **Student**: Manages student profiles and their associations with classrooms, parents, and subjects.
- **Subject**: Contains information about subjects taught in the school.
- **Teacher**: Manages teacher profiles, including subjects they teach and classrooms they manage.
- **User**: Represents system users with roles (Admin, Teacher, Student, Parent).

## Project Structure
```CSS
    ├── src 
    │     ├── main 
    │     │     ├── java 
    │     │     │     └── com 
    │     │     │           └── studentmanagementsystem 
    │     │     │                 ├── entity                      # Entity classes
    │     │     │                 │     ├── Address.java
    │     │     │                 │     ├── Classroom.java
    │     │     │                 │     ├── Homework.java
    │     │     │                 │     ├── Parent.java
    │     │     │                 │     ├── Report.java
    │     │     │                 │     ├── School.java
    │     │     │                 │     ├── Student.java
    │     │     │                 │     ├── Subject.java
    │     │     │                 │     ├── Teacher.java
    │     │     │                 │     └── Users.java
    │     │     │                 │
    │     │     │                 ├── repository                  # Repository interfaces
    │     │     │                 │     ├── AddressRepository.java
    │     │     │                 │     ├── ClassroomRepository.java
    │     │     │                 │     ├── HomeworkRepository.java
    │     │     │                 │     ├── ParentRepository.java
    │     │     │                 │     ├── ReportRepository.java
    │     │     │                 │     ├── SchoolRepository.java
    │     │     │                 │     ├── StudentRepository.java
    │     │     │                 │     ├── SubjectRepository.java
    │     │     │                 │     ├── TeacherRepository.java
    │     │     │                 │   └── UsersRepository.java
    │     │     │                 │
    │     │     │                 ├── service                     # Service interfaces
    │     │     │                 │     ├── AddressService.java
    │     │     │                 │     ├── ClassroomService.java
    │     │     │                 │     ├── HomeworkService.java
    │     │     │                 │     ├── ParentService.java
    │     │     │                 │     ├── ReportService.java
    │     │     │                 │     ├── SchoolService.java
    │     │     │                 │     ├── StudentService.java
    │     │     │                 │     ├── SubjectService.java
    │     │     │                 │     ├── TeacherService.java
    │     │     │                 │     ├── UsersService.java
    │     │     │                 │     └── impl                    # Service implementation classes
    │     │     │                 │           ├── AddressServiceImpl.java
    │     │     │                 │           ├── ClassroomServiceImpl.java
    │     │     │                 │           ├── HomeworkServiceImpl.java
    │     │     │                 │           ├── ParentServiceImpl.java
    │     │     │                 │           ├── ReportServiceImpl.java
    │     │     │                 │           ├── SchoolServiceImpl.java
    │     │     │                 │           ├── StudentServiceImpl.java
    │     │     │                 │           ├── SubjectServiceImpl.java
    │     │     │                 │           ├── TeacherServiceImpl.java
    │     │     │                 │           └── UsersServiceImpl.java
    │     │     │                 │
    │     │     │                 └── controller                  # REST controllers
    │     │     │                      ├── AddressController.java
    │     │     │                      ├── ClassroomController.java
    │     │     │                      ├── HomeworkController.java
    │     │     │                      ├── ParentController.java
    │     │     │                      ├── ReportController.java
    │     │     │                      ├── SchoolController.java
    │     │     │                      ├── StudentController.java
    │     │     │                      ├── SubjectController.java
    │     │     │                      ├── TeacherController.java
    │     │     │                      └── UsersController.java
    │     │     │
    │     │     └── resources                             # Resources directory
    │     │           ├── application.properties
    │     │           ├── application-mysql.properties
    │     │           ├── application-plsql.properties
    │     │           ├── applicationazure_sql.properties
    │     │           ├── application-mongo.properties
    │     │           ├── application-h2.properties
    │     │           └── templates                         # Thymeleaf templates
    │     │
    │     └── test                                      # Test directory
    │           └── java 
    │                 └── com 
    │                       └── studentmanagementsystem 
    │                             └── (Test Classes)            # Test classes for unit and integration testing
    │
    └── pom.xml                                       # Maven Project Object Model file
```
## Getting Started

### Prerequisites
- **Java 17** or higher
- **Maven**: For building and managing project dependencies.
- **MySQL/PostgreSQL/AzureSQL/MongoDB**: Depending on your database choice.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/harshitasharma77/StudentManagementSystem.git
   cd student-management-system
   ```

2. **Setup the database:**
    - Configure your database of choice (MySQL, PostgreSQL, AzureSQL, or MongoDB).
    - Update the `application.properties` or `application.yml` file in the `src/main/resources` directory with your database credentials.

3. **Build the project:**
   ```bash
   mvn clean install
   ```

4. **Run the application:**
   ```bash
   mvn spring-boot:run
   ```

### Running Tests
- **In-Memory Database Testing**: The project is configured to use the H2 database for testing.
  ```bash
  mvn test
  ```

## Usage

- **Access the application**:
  Open a web browser and navigate to `http://localhost:9090` to start using the application.

- **Admin Dashboard**:
  Administrators can manage students, teachers, subjects, and more.

- **Teacher Dashboard**:
  Teachers can manage their assigned classes, assign homework, and track student progress.

- **Student and Parent Portals**:
  Students and parents can view homework, reports, and other relevant information.

[//]: # (## Deployment)

[//]: # ()
[//]: # (### Azure Deployment)

[//]: # (- The application can be deployed on Microsoft Azure using Azure App Services and Azure SQL.)

[//]: # (### Docker)

[//]: # (- A Dockerfile is included for containerization.)

[//]: # (  ```bash)

[//]: # (  docker build -t student-management-system .)

[//]: # (  docker run -p 8080:8080 student-management-system)

[//]: # (  ```)

[//]: # (## Contributing)

[//]: # (Contributions are welcome! Please follow the standard [GitHub flow]&#40;https://guides.github.com/introduction/flow/&#41; for submitting pull requests.)

[//]: # (## License)

[//]: # (This project is licensed under the MIT License. See the [LICENSE]&#40;LICENSE&#41; file for more details.)

---
