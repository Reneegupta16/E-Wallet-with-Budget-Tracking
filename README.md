# E-Wallet-with-Budget-Tracking
This Spring Boot application is a fully functioning Personal Finance Management System designed to help users manage their finances by tracking incomes and expenses. The application includes user registration, authentication, transaction management, and basic error handling, all implemented using a RESTful service architecture. The backend is built with Java Spring Boot, leveraging JPA for database interactions and Spring Security for authentication and authorization.

Project Structure

The project follows a standard Spring Boot structure, organized into several packages to promote modularity and maintainability:

 • config: Configuration classes, including security configurations.
 • controller: REST controllers that handle HTTP requests and responses.
 • model: Entity classes representing the database schema.
 • repository: JPA repository interfaces for data access.
 • service: Service classes containing business logic.
 • security: Security-related classes, including JWT handling.

Main Components

User Registration and Authentication

 • User Registration: Allows users to register by providing a username and password. Passwords are securely stored using BCrypt hashing.
 • Authentication: Utilizes JWT (JSON Web Tokens) for stateless authentication. Users can log in with their credentials, and the application issues a JWT that must be included in subsequent requests for authentication.

Transaction Management

 • Income and Expense Tracking: Users can add, view, and manage their financial transactions, categorized as either income or expenses.
 • Real-time Data: Transactions are stored in an H2 in-memory database for simplicity, which can be switched to a more robust database like PostgreSQL for production use.

Security

 • JWT Security: Ensures that only authenticated users can access the application’s endpoints, protecting user data and functionality from unauthorized access.
 • Password Encryption: Uses BCrypt to securely hash and store user passwords.

Configuration and Dependencies

The application is configured through application.properties and relies on several key dependencies, including:

 • Spring Boot Starter Data JPA: For database interactions.
 • Spring Boot Starter Security: For securing the application.
 • H2 Database: An in-memory database for development and testing.
 • Lombok: To reduce boilerplate code (optional).
 • JWT (Java JSON Web Tokens): For handling token-based authentication.
