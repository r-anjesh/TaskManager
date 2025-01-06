**Task Manager Web Application**
=====================================

**Overview**
------------

This project is a Task Manager Web Application developed using Node.js, Express.js, MongoDB, and a frontend built with HTML, CSS, and JavaScript. The application allows users to register, log in, and manage tasks efficiently through CRUD (Create, Read, Update, Delete) operations.

**Features**
------------

* User Registration and Login (JWT-based Authentication)
* CRUD Operations for Task Management
* Responsive Frontend (Mobile and Desktop Support)
* Secure and Efficient Backend with Error Handling and Validation
* Integration with MongoDB for Data Persistence

**Table of Contents**
-----------------

* [Installation](#installation)
* [Technologies Used](#technologies-used)
* [API Endpoints](#api-endpoints)
* [Frontend Setup](#frontend-setup)
* [Backend Setup](#backend-setup)
* [Running the Application](#running-the-application)
* [Testing](#testing)

**Installation**
------------

### Prerequisites

* Ensure that you have the following installed:
	+ Node.js (v14 or above)
	+ npm (Node Package Manager)
	+ MongoDB (or a cloud-based MongoDB service like MongoDB Atlas)

### Steps

1. Clone the Repository
```bash
git clone https://github.com/r-anjesh/task-manager.git
```
2. Backend Setup
```bash
cd backend
npm install
```
Create a `.env` file in the backend folder and add the following variables:
```makefile
MONGO_URI=mongodb+srv://<your-username>:<your-password>@cluster0.owpch.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
JWT_SECRET=<your-secret-key>
CLIENT_URL=http://localhost:3000
PORT=8000
```
Replace `<your-username>` and `<your-password>` with your actual MongoDB username and password.

3. Frontend Setup
```bash
cd frontend
npm install
```
4. Running the Application
```bash
# Backend
npm start
# Frontend
npm start
```
**Technologies Used**
-------------------

* Frontend: HTML, CSS, JavaScript (React.js or plain JS)
* Backend: Node.js, Express.js
* Database: MongoDB
* Authentication: JWT (JSON Web Tokens)
* Other Libraries/Tools: bcryptjs, dotenv, mongoose, cors

**API Endpoints**
----------------

### User Authentication

* POST /api/auth/register: Register a new user
* POST /api/auth/login: Log in and get a JWT token
* GET /api/auth/me: Get user details (protected route)

### Task Management

* POST /api/tasks: Create a new task (Protected Route)
* GET /api/tasks: Get all tasks (Protected Route)
* GET /api/tasks/:id: Get a specific task (Protected Route)
* PUT /api/tasks/:id: Update a task (Protected Route)
* DELETE /api/tasks/:id: Delete a task (Protected Route)

**Frontend Setup**
-----------------

* Registration and Login Forms: Allow users to register and log in to the app using JWT authentication.
* Task Management Interface: Displays tasks in a list, and provides buttons for adding, editing, and deleting tasks.
* Responsive Design: Ensures the app is usable on different screen sizes.

**Backend Setup**
-----------------

* JWT Authentication: Protect the task management routes by verifying the JWT in the authorization header.
* Error Handling: Handle errors appropriately and provide meaningful error messages to users.
* MongoDB Integration: Store user and task data in a MongoDB database using mongoose.

**Running the Application**
---------------------------

### Development Mode

* To run the frontend and backend locally, follow the steps in the Installation section and execute both the frontend and backend.

### Production Mode

* You can deploy both the frontend and backend to platforms like Heroku, Netlify, or Vercel for production hosting.
* For MongoDB, you can use MongoDB Atlas for cloud-based database hosting.

**Testing**
------------

* The backend includes basic API testing for validation and error handling.
* You can use Postman to test the API endpoints manually.
* For unit testing, you can integrate Jest and Supertest to automate the testing of the backend.

