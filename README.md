The project contains the following primary microservices:
Auth Service
Email Service
Hotel Service
Room Service
User Service

Common Technologies and Tools :
Java with Spring Boot
Maven for project management (pom.xml)
Layered Architecture: DTO, Entity, Service, Repository, Controller
RESTful API Design
Exception Handling with custom exception classes
Possibly uses JWT / Spring Security for authentication
Microservices pattern: each feature runs as an independent module, scalable and maintainable

Detailed Description of Each Service
1. Auth Service
Purpose: Handles user authentication and authorization.
Key Components:
DTO classes for login and auth requests.
Controllers to handle login/logout endpoints.
Services to manage token generation (possibly using JWT).
Exception handling for invalid credentials or user not found.
Spring Security configuration (likely included under config/).

2. Email Service
Purpose: Sends emails (probably for notifications like password reset, booking confirmation).
Key Components:
dto for email content (subject, body, recipient).
A controller to expose API for sending emails.
Service for SMTP or third-party email integration (like SendGrid or JavaMailSender).

3. Hotel Service
Purpose: Manages hotels’ data.
Key Components:
entity classes for hotels.
repository layer to access hotel data.
Controller and service to manage hotel creation, update, delete, and fetch operations.
Custom exceptions (e.g., HotelNotFoundException).

 4. Room Service
Purpose: Manages room-related operations within hotels.
Key Components:
DTOs to describe room features, pricing, etc.
Entity models representing room objects.
Controller and service logic for room availability, booking, etc.
Repository to interact with the database.

5. User Service
Purpose: Manages user registration, profile, and personal data.
Key Components:
DTOs for user input and output.
Entity models for storing user data (name, email, roles, etc.).
Controller and service for handling user APIs.
Exception handling for user-related issues (e.g., duplicate email, user not found).

