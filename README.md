# Spring Boot User Registration Application

This is a simple user registration application built with Spring Boot, Spring Security, and JSP.

## Project Structure

```
src/main/java/com/example/userregistration/
├── UserRegistrationApplication.java
├── config/
│   └── SecurityConfig.java
├── controller/
│   └── UserController.java
├── model/
│   └── User.java
└── repository/
    └── UserRepository.java

src/main/webapp/WEB-INF/jsp/
└── register.jsp

src/main/resources/
└── application.properties
```

## Features

- User registration with username, password, and email
- Password encryption using BCrypt
- Form validation
- JSP view with Bootstrap styling
- H2 in-memory database
- Spring Security integration

## Prerequisites

- Java 11 or higher
- Maven 3.6 or higher

## How to Run

1. Clone the repository
2. Navigate to the project directory
3. Run the application:
   ```bash
   mvn spring-boot:run
   ```
4. Access the application at `http://localhost:8080/register`

## Security Features

- Passwords are encrypted using BCryptPasswordEncoder
- Form validation for username and email uniqueness
- CSRF protection enabled
- Secure password storage

## JSP Tags Used

- `<form:form>`: Spring form tag for form handling
- `<form:input>`: Input field binding
- `<form:password>`: Password field binding
- `<form:errors>`: Display validation errors
- `<c:if>`: Conditional rendering
- `<c:out>`: Output escaping

## Database

The application uses H2 in-memory database. You can access the H2 console at:
`http://localhost:8080/h2-console`

Database credentials:
- JDBC URL: `jdbc:h2:mem:userdb`
- Username: `sa`
- Password: (empty)

## API Endpoints

- GET `/register`: Display registration form
- POST `/register`: Process registration form

## Error Handling

The application handles the following cases:
- Duplicate username
- Duplicate email
- Invalid form data
- Server errors 