# Backend Requirement Specifications – ALX Airbnb Project

This document outlines the technical and functional requirements for key backend features of the ALX Airbnb platform. The focus is on **User Authentication**, **Property Management**, and **Booking System**.

---

## 1. User Authentication

### Description
Provides secure login, registration, and session management for users (guests and hosts).

### API Endpoints
- **POST /api/v1/auth/register**
  - Registers a new user.
- **POST /api/v1/auth/login**
  - Authenticates a user and issues a JWT token.
- **GET /api/v1/auth/profile**
  - Retrieves current user’s profile (requires authentication).
- **POST /api/v1/auth/logout**
  - Logs out the user and invalidates the token.

### Input Specifications
- **Register**
  ```json
  {
    "name": "John Doe",
    "email": "john@example.com",
    "password": "securePassword123",
    "role": "host"   // or "guest"
  }
