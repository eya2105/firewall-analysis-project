# Firewall Log Analysis Platform

A modular full-stack firewall log analysis platform built with **NestJS**, **Angular**, and **PostgreSQL**. The platform enables organizations to securely collect, normalize, analyze, and visualize firewall logs from multiple vendors, providing advanced search capabilities, anomaly detection, interactive dashboards, and automated report generation.

The system is designed with a modular architecture, allowing each component to evolve independently while integrating into a secure and scalable cybersecurity platform.

## Project Features

- Secure JWT-based authentication and authorization
- User and role management
- Firewall log import and normalization
- Support for multiple firewall vendors
- Advanced log search and filtering
- Anomaly detection and security analysis
- Interactive dashboards and statistics
- CSV/PDF report generation
- Audit logging for authentication events
- Modular and extensible architecture

---

# My Contribution

I was responsible for designing and implementing the **Identity and Access Management (IAM)** layer of the platform, which provides the authentication, authorization, and security foundation for the entire backend.

This component ensures that every protected resource in the system is accessed securely while providing centralized user management, permission control, and authentication auditing.

## Authentication

Implemented a complete JWT-based authentication system including:

- User login and registration
- Access and refresh token generation
- Refresh token rotation
- Secure logout
- Protected user profile endpoints
- Hashed refresh token storage

## Authorization

Designed a flexible authorization layer based on both roles and permissions.

Features include:

- Global authentication guard
- Role-Based Access Control (RBAC)
- Permission-Based Access Control (PBAC)
- Public route support
- Custom decorators for roles, permissions, and current user extraction
- JWT validation pipeline for protected endpoints

## User & Account Security

Implemented secure user management features including:

- User creation and administration
- User update and profile management
- Password change workflows
- Account locking and unlocking
- Failed login attempt tracking
- Soft delete and account restoration
- Protection against deleting the last administrator
- Protection against administrator privilege downgrade

## Authentication Audit

Developed a complete authentication auditing system to improve traceability and security monitoring.

Tracked events include:

- Successful logins
- Failed login attempts
- Logout events
- Token refresh operations
- Account lock events
- Brute-force detection
- Authentication history for auditing and monitoring

## System Infrastructure

Implemented the shared security infrastructure used across the backend:

- Centralized environment-based configuration
- Base entities for timestamps and soft deletion
- Administrator database seed script
- Shared enums, constants, interfaces, and decorators

## Project Structure

```
src/
├── auth/          # Authentication, JWT, guards, strategies and decorators
├── users/         # User management and account security
├── authaudit/     # Authentication audit logging
├── common/        # Shared enums, constants, base entities and utilities
└── config/        # Application configuration
```

## Security Highlights

- Passwords are securely hashed before storage
- Refresh tokens are hashed and rotated
- JWTs are validated against user status and account lock state
- Access control is enforced through roles and permissions
- Authentication events are fully auditable
- Soft deletion prevents accidental data loss
- Critical administrator accounts are protected against unsafe operations
- Security settings are configurable through environment variables

---

## Outcome

This contribution establishes the secure identity and access management layer of the platform, providing authentication, authorization, account protection, and security auditing for all backend services. It serves as the entry point to every protected feature within the application while ensuring secure, traceable, and maintainable access control.
