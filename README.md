# Backend Project README

This README.md file provides an overview and instructions for a backend project that implements a CRUD API using Express.js, JavaScript, JWT (JSON Web Tokens), MongoDB, and middleware.

## Project Overview

The backend project aims to create a RESTful API with CRUD functionality. It uses Express.js, a popular web application framework for Node.js, to handle routing and HTTP requests. MongoDB is chosen as the database for storing and retrieving data. JWT is used for authentication and authorization. Middleware is employed to perform additional tasks such as request validation, error handling, and logging.

## Project Setup

To set up the project, follow the steps below:

1. Make sure you have Node.js and npm (Node Package Manager) installed on your machine.

2. Clone the project repository from GitHub:

   ```bash
   git clone https://github.com/bar2693lis/simple-backend-project.git
   ```

3. Navigate to the project directory:

   ```bash
   cd mycontact-backend
   ```

4. Install project dependencies:

   ```bash
   npm install
   ```

5. Create a `.env` file in the root directory of the project and provide the necessary environment variables:

   ```plaintext
   PORT=3000
   CONNECTION_STRING=<your_mongodb_uri>
   ACCESS_TOKEN_SECRET=<your_jwt_secret>
   ```

   Make sure to replace `<your_mongodb_uri>` with the actual connection string for your MongoDB database and `<your_jwt_secret>` with a secure secret key for JWT token signing.

6. Start the server:

   ```bash
   npm start
   ```

   This command will start the server at `http://localhost:3000`.

## Project Structure

The project's file structure may look similar to the following:

```plaintext
mycontact-backend/
├── config/
│   └── dbConnection.js
├── controllers/
│   ├── contactController.js
│   └── userController.js
├── middleware/
│   ├── errorHandler.js
│   └── validateTokenHandler.js
├── models/
│   ├── contactModel.js
│   └── userModel.js
├── routes/
│   ├── contactRoutes.js
│   └── userRoutes.js
├── .env
├── server.js
├── constants.js
├── package.json
└── README.md
```

- `controllers/`: Contains controller modules that handle different API endpoints or routes.
- `middleware/`: Holds middleware modules responsible for request validation, error handling, and more.
- `models/`: Consists of data models defining the structure and operations for MongoDB documents.
- `routes/`: Contains route modules that define the API endpoints and associated controllers.
- `.env`: Configuration file for environment variables.
- `server.js`: The main entry point of the application where Express.js and middleware are configured.
- `constants.js`: Contains the errors code.
- `package.json`: Contains project metadata and lists dependencies.

## API Endpoints

The following API endpoints are available in this project:

### Data

- **GET** `/api/contacts`: Get all data.
- **POST** `/api/contacts`: Create a new data.
- **GET** `/api/contacts/:id`: Get a specific data entry.
- **PUT** `/api/contacts/:id`: Update a specific data entry.
- **DELETE** `/api/contacts/:id`: Delete a specific data entry.

- **POST** `/api/users/register`: Create a new data.
- **POST** `/api/users/login`: Get a specific data entry.
- **GET** `/api/users/current`: Get a specific data entry.

## Middleware

The project includes the following middleware:

- `validateTokenHandler.js`: Handles authentication using JWT tokens.
- `errorHandler.js`: Catches and handles errors thrown during request processing.

## Conclusion

This README.md file provided an overview and setup instructions for a backend project implementing a CRUD API using Express.js, JavaScript, JWT, MongoDB
