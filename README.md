# Template-backend

This is a template project with basic configurations to kickstart a backend project in Java using Spring Boot and Maven. The template follows a well-defined layered architecture and includes several key features to help streamline development:

*   Custom exceptions: A set of tailored exception classes for better error handling.
*   Model Mapper: Configured for object-to-object mapping, simplifying data transformation.
*   Example Validations: Regex-based validations for common input checks.
*   Swagger Integration: Pre-configured for API documentation and testing.
*   Unit Tests: Tests written with Mockito and JUnit to ensure code reliability and coverage.
*   Flyway Migration: Configured for fast database initialization with version-controlled migrations.
*   H2 Database: Set up for in-memory testing and development environments.
*   PostgreSQL Configuration: Integrated for production-grade database management.
*   Lombok: Integrated for reducing boilerplate code by automatically generating getters, setters, constructors, and other utility methods.
*   Dockerfile: Pre-configured for containerizing the application and simplifying deployment with Docker.
*   Property Management: Clean separation of development and production properties for better configuration management.

This template is designed to help developers quickly set up a robust backend application with standardized configurations and best practices, making it easy to scale and maintain.

## Environment Setup for the Backend

Requirements:

* JDK 17+
* Apache Maven 3.9.2 
* Preferably IntelliJ
* OS: Preferably win32 x64

Instructions:

1- Install the JDK by downloading it from the official Oracle website, or an equivalent.
  * Use the installer, or if you choose the ZIP, you will need to configure the environment variables.
  * Verify that the JDK version was installed correctly with the command ```java -version```
  
2- Install Maven
  * If you choose the ZIP, you will need to configure the environment variables.
  * Verify that the Maven version was installed correctly with the command ```mvn -v```

3- Clone the project from the repository to a folder of your choice.
  * Open the chosen folder in IntelliJ or your preferred IDE, then navigate to the backend directory and wait for the IDE's indexing process to complete.
  * Start the project by running the BackendApplication main class;
  * If the Maven dependencies are not loaded correctly, run the command on your terminal ```mvn clean package install```
  * By default, the application will be available on port 8080

# Testing the Application
You can test the main features of the application via:
  * Swagger: **http://localhost:8080/swagger-ui/index.html** where you can test all application endpoints.
  * H2-BD: **http://localhost:8080/h2-console/** where you can acess you DB if you have H2 console activated on dev properties

**Note** The application is associated with an H2 in-memory database, so there is no need to configure an external database. The creation of tables and database population is also implemented in the application using Flyway.
