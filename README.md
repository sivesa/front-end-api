# Login and Registration API

## Overview
This API provides front-end functionality for user authentication and registration. It supports traditional username-password authentication as well as social login options via Google and Facebook. The API is implemented using JavaScript and utilizes asynchronous functions for network operations.

## Features
- **User Login**: Authenticate users using user identifier and password or through social login options.
- **User Registration**: Register new users with their personal details or through social platforms.
- **Password Validation**: Ensures passwords match during registration.
- **Error Handling**: Alerts users to failed login/registration attempts and logs errors to the console.

## Login Implementation

### Login with Membership Number
**Function:** `loginUser()`

**Description:** Authenticates users based on their identifier and password.

**Workflow:**
1. Retrieves the identifier and password from input fields.
2. Sends a `POST` request to the `/api/api/login` endpoint with form-encoded data.
3. Redirects users to the landing page on successful authentication or displays an error message on failure.

### Social Login
- **Google Login:** Redirects users to `/api/auth/google` for authentication.
- **Facebook Login:** Redirects users to `/api/auth/facebook` for authentication.

## Registration Implementation

### Register with Personal Details
**Function:** `registerUser()`

**Description:** Registers new users by collecting their personal details and ensuring password confirmation.

**Workflow:**
1. Collects first name, last name, email, password, and password confirmation from input fields.
2. Validates that the `password` and `repeatPassword` fields match.
3. Sends a `POST` request to the `/api/register` endpoint with form-encoded data.
4. Redirects users to the landing page on successful registration or displays an error message on failure.


### Social Registration
- **Google Registration:** Redirects users to `/api/auth/google` for registration.
- **Facebook Registration:** Redirects users to `/api/auth/facebook` for registration.

## Getting Started

### Prerequisites
- A basic understanding of JavaScript and asynchronous programming.
- A development environment capable of running a local web server.

### Running the Application
1. Clone the repository:
   ```bash
   git clone https://github.com/sivesa/front-end-api.git
   ```
2. Navigate to the project directory:
   ```bash
   cd front-end-api
   ```
3. Serve the application using a local server (e.g., Live Server for VS Code).

## Security Considerations
- Always use HTTPS for secure communication.
- Implement server-side password hashing (e.g., bcrypt).
- Include rate limiting to prevent brute-force attacks.

## License
This project is licensed under the MIT License.

