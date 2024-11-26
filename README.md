
# RBAC MERN Stack Project

This is a basic implementation of a Role-Based Access Control (RBAC) system using the MERN stack (MongoDB, Express, React, and Node.js). The project allows users to register with specific roles, log in, and access protected routes based on their roles.

---

## Features

- User Signup and Login functionality.
- Role-Based Access Control for protected routes.
- JWT-based authentication for secure API calls.

---

## Prerequisites

- [Node.js](https://nodejs.org) installed.
- [MongoDB](https://www.mongodb.com) installed or access to a MongoDB cloud instance (e.g., MongoDB Atlas).

---

## Installation

### 1. Clone or Extract the Project
Download and extract the project files or clone the repository if available.

### 2. Setup Backend (`server`)
1. Navigate to the `server` directory:
   ```bash
   cd server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the `server` directory and add the following:
   ```env
   MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/rbac-app
   JWT_SECRET=your_jwt_secret
   ```
   - Replace `<username>` and `<password>` with your MongoDB credentials.
   - Replace `your_jwt_secret` with a secure secret key.

4. Start the server:
   ```bash
   npm start
   ```
   The server will run on `http://localhost:5000`.

### 3. Setup Frontend (`client`)
1. Navigate to the `client` directory:
   ```bash
   cd client
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the client:
   ```bash
   npm start
   ```
   The client will run on `http://localhost:3000`.

---

## Usage

### 1. Open the Application
Access the frontend at `http://localhost:3000`.

### 2. Signup
Go to `/signup` and create a user account with a role.

### 3. Login
Log in at `/login` with the credentials you created.

### 4. Dashboard
After logging in, access the `/dashboard`. Role-based access can be extended as needed.

---

## Project Structure

```
RBAC-MERN-Project/
├── server/
│   ├── models/           # MongoDB models for User and Role
│   ├── routes/           # Express routes for authentication
│   ├── middleware/       # Middleware for authentication and authorization
│   ├── server.js         # Main server file
│   └── .env              # Environment variables for secrets and DB connection
└── client/
    ├── src/
    │   ├── components/   # React components (Login, Signup, Dashboard)
    │   ├── App.js        # React application entry point
    │   └── index.js      # React rendering logic
```

---

## API Endpoints

### Auth Routes
- `POST /api/auth/signup`: Create a new user.
- `POST /api/auth/login`: Authenticate a user and return a JWT.

---

## Technologies Used

- **Backend**: Node.js, Express.js, MongoDB, Mongoose.
- **Frontend**: React.js, Axios, React Router.

---

## Future Enhancements

- Add user management for administrators.
- Implement role and permission management.
- Improve UI with a frontend framework (e.g., Material-UI or Bootstrap).

---

## License

This project is licensed under the MIT License.
