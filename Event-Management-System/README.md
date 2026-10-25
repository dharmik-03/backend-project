# Event Management System — Backend

A Node.js backend application for managing event-related data through a modular API architecture. The project separates routes, controllers, models, database configuration, and middleware to keep the code organized and maintainable.

## Overview

The Event Management System backend provides the foundation for handling event-related operations, with dedicated modules for event routes, event controllers, data models, database configuration, and file uploads.

## Features

- **Event Management** — Dedicated event controller and model for event-related operations.
- **REST API Routes** — Separate route module for handling event requests.
- **Database Configuration** — Dedicated database configuration file.
- **File Upload Middleware** — Reusable middleware for handling file uploads.
- **Centralized HTTP Error Handling** — Dedicated middleware for handling HTTP errors.
- **Modular Architecture** — Organized controllers, routes, models, and configuration.
- **Environment Configuration** — Environment variables for application settings and credentials.

## Technology Stack

- **Node.js** — JavaScript runtime.
- **JavaScript** — Backend application logic.
- **Database** — Configured through `config/db.js`; confirm the database type in your implementation.
- **npm** — Package and dependency management.

## Project Structure

```text
Event-Management-System/
├── config/
│   └── db.js
├── controller/
│   └── EventController.js
├── middlewares/
│   ├── httpError.js
│   └── upload.js
├── model/
│   └── eventModel.js
├── routes/
│   └── eventRoute.js
├── .env
├── .gitignore
├── package-lock.json
├── package.json
└── server.js
```

## Getting Started

### Prerequisites

- Node.js installed on your system.
- npm installed with Node.js.
- Access to the database configured by the application.

### 1. Install Dependencies

Open a terminal in the project directory and run:

```bash
npm install
```

### 2. Configure Environment Variables

Create a `.env` file in the project root and add the variables required by your application.

Example:

```env
PORT=5000
DATABASE_URL=your_database_connection_string
```

These are example placeholders. Use the exact variable names expected by your `config/db.js` and `server.js` files.

### 3. Start the Server

If `package.json` does not define a start script, run:

```bash
node server.js
```

For development, if Nodemon is installed:

```bash
npx nodemon server.js
```

### 4. Test the API

Use Postman or another API client to test the endpoints defined in `routes/eventRoute.js`.

Check the route and controller files for the actual HTTP methods, endpoint paths, request formats, and response structures.

## CRUD Operations

CRUD stands for Create, Read, Update, and Delete.

| Operation | HTTP Method | Purpose |
|---|---|---|
| Create | POST | Create an event |
| Read | GET | Retrieve event information |
| Update | PUT / PATCH | Modify event information |
| Delete | DELETE | Delete an event |

The project includes an event route, controller, and model. The table describes standard event-management operations; verify which operations are actually implemented in your code.

## Error Handling and Middleware

- **`httpError.js`** — Dedicated HTTP error-handling middleware.
- **`upload.js`** — Middleware for file uploads.
- **`db.js`** — Database configuration.
- **`eventRoute.js`** — Event API route definitions.
- **`EventController.js`** — Event request handling.
- **`eventModel.js`** — Event data model.

## Security

- Keep database credentials and other secrets in `.env`.
- Ensure `.env` is excluded through `.gitignore`.
- Never upload passwords, API keys, or private credentials to GitHub.
- Validate incoming request data before processing it.
- Restrict file uploads by type and size where appropriate.

## Future Improvements

- Document all API endpoints and request/response examples.
- Add request validation and automated testing.
- Implement pagination and filtering for event listings.
- Add authentication and authorization if required.
- Add API documentation using Swagger or OpenAPI.
- Introduce structured logging and production monitoring.

## Author

**Dharmik**

