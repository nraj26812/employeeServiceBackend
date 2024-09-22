
# Employee Service Module - Backend

This repository contains the backend for the **Employee Service Module** built using **Java Spring Boot** and **PostgreSQL**. It is designed to manage employee data within a shopping mall environment, allowing CRUD operations and efficient management of employee details.

## Project Structure

The project follows a typical **Spring Boot** structure with clearly defined layers:

- **Controller Layer**: Handles HTTP requests and directs them to the appropriate service.
- **Service Layer**: Contains business logic for handling employee operations.
- **Repository Layer**: Manages interaction with the PostgreSQL database through JPA.

## Features

- Create, read, update, and delete employee records.
- Integration with **PostgreSQL** for persistent data storage.
- API-based communication between the front-end and back-end.
- Input validation and exception handling for robust data processing.

## Technologies Used

- **Java 17** (or later)
- **Spring Boot**
- **Spring Data JPA**
- **PostgreSQL**
- **Maven** (for dependency management)
- **Postman** (for API testing)

## Setup Instructions

### Prerequisites

- Java 17 or higher installed
- PostgreSQL database installed
- Maven installed

### Step-by-Step Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/nraj26812/employeeservice.git
   cd employeeservice
   ```

2. **Configure PostgreSQL:**

   - Create a PostgreSQL database (e.g., `employee_db`).
   - Update the `application.properties` or `application.yml` file with your database credentials:

     ```properties
     spring.datasource.url=jdbc:postgresql://localhost:5432/employee_db
     spring.datasource.username=your_db_username
     spring.datasource.password=your_db_password
     spring.jpa.hibernate.ddl-auto=update
     ```

3. **Build and run the application:**

   Use Maven to build and start the application:

   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

4. **Access the application:**

   - The application will be running on `http://localhost:8080`.
   - API documentation is available via Swagger at `http://localhost:8080/swagger-ui.html`.

## API Endpoints

The following endpoints are available for interacting with the Employee Service module:

| Method | Endpoint             | Description                        |
|--------|----------------------|------------------------------------|
| GET    | `/employees`         | Fetch all employees                |
| GET    | `/employees/{id}`    | Fetch a single employee by ID      |
| POST   | `/employees`         | Add a new employee                 |
| PUT    | `/employees/{id}`    | Update an employee by ID           |
| DELETE | `/employees/{id}`    | Delete an employee by ID           |

## Testing

- Use **Postman** or **Swagger** to test the API endpoints.
- Example request payload for creating a new employee:

  ```json
  {
    "name": "John Doe",
    "position": "Sales Manager",
    "salary": 55000,
    "department": "Sales"
  }
  ```

## Contribution Guidelines

Feel free to submit issues or create pull requests if you have suggestions for improvements. Please ensure that any new functionality is covered by tests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
