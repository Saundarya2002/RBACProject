# RBACProject
Role-Based Access Control (RBAC) with Authentication and JWT
Overview
This project demonstrates the implementation of Role-Based Access Control (RBAC), Authentication, and Authorization using JWT (JSON Web Tokens) in a Java application. The system allows users to register, log in, and log out securely, with access control based on the user's role. The roles include Admin, Editor, and Viewer, each having specific permissions to access different resources or endpoints.

Features
User Authentication: Secure login using hashed passwords.
Role-Based Access Control (RBAC): Users are assigned roles such as Admin, Editor, or Viewer, which define what they can access.
JWT Authentication: Secure token generation for session management.
Secure Password Handling: Passwords are hashed using BCrypt for security.
UI for Login and Role-based Dashboards: A simple user interface to log in and show dashboards based on the user's role.

Login with Predefined Users
You can use the following credentials to log in:

Admin

Username: admin
Password: admin123
Editor

Username: editor
Password: editor123
Viewer

Username: viewer
Password: viewer123
Each user is assigned a role and will be redirected to a role-specific dashboard after login.

How It Works
1. User Registration
Users can be added directly into the database via SQL scripts (schema.sql).
Passwords are hashed using BCrypt to ensure secure storage.
2. Authentication
When a user logs in, the system compares the entered password with the hashed password stored in the database.
If the credentials are correct, a JWT token is generated containing the user's role.
3. Authorization (RBAC)
Based on the role assigned to the user (Admin, Editor, or Viewer), different pages or resources are accessible.
Admin has the highest level of access, Editor can modify certain resources, and Viewer has read-only access.
4. JWT for Session Management
Once logged in, a JWT is generated for the user. This token is then used for validating subsequent requests, ensuring that the user has the proper permissions to access different resources.
Dependencies
The project uses the following dependencies:

Spring Boot (for dependency management and running the application)
JWT (for token management)
BCrypt (for hashing passwords)
H2 Database (for storing user data)
