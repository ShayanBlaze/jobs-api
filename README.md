# 🚀 Jobs API

[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)
[![Made with: Node.js](https://img.shields.io/badge/Made%20with-Node.js-1f425f.svg)](https://nodejs.org/)
[![Documentation: Swagger UI](https://img.shields.io/badge/Documentation-Swagger%20UI-brightgreen)](https://jobs-api-w9hs.onrender.com/api-docs)

Hello! Welcome to the **Jobs API** documentation. This project is a powerful and secure API for managing job postings and application processes, built with Node.js and Express.js.

This API allows users to register, log in, and then manage their own job listings (create, read, update, and delete).

✨ **[View the Live Demo](https://jobs-api-w9hs.onrender.com/)** ✨

![Swagger UI Demo](https://i.imgur.com/gEhNnSg.png)

> **Note:** The image above shows a preview of the interactive Swagger UI documentation for this project.

---

## 📚 Full API Documentation

To see the complete list of endpoints, required parameters, and to test the API directly, please visit our interactive documentation built with **Swagger UI**:

➡️ **[Link to Interactive API Docs](https://jobs-api-w9hs.onrender.com/api-docs)**

---

## 🛠️ Tech Stack

This project was built using the latest and most popular technologies in the Node.js ecosystem:

- **Core Framework:** [Express.js](https://expressjs.com/)
- **Database:** [MongoDB](https://www.mongodb.com/) with [Mongoose](https://mongoosejs.com/) for object data modeling
- **Authentication:** [JSON Web Tokens (JWT)](https://jwt.io/) for secure user sessions
- **Security:**
  - `bcrypt.js`: For secure password hashing
  - `helmet`: To secure HTTP headers
  - `cors`: To enable Cross-Origin Resource Sharing
  - `xss-clean`: To prevent Cross-Site Scripting (XSS) attacks
  - `express-rate-limit`: To limit repeated requests and prevent brute-force attacks
- **Documentation:** [Swagger UI](https://swagger.io/tools/swagger-ui/)
- **Error Handling:** Custom middleware for handling 404 and 500 errors

---

## 📂 Project Structure

The file and folder structure is designed for easy readability and maintainability:

```
JOBS-API/
├── controllers/
│   ├── auth.js
│   └── jobs.js
├── db/
│   └── connect.js
├── errors/
│   ├── bad-request.js
│   ├── custom-api.js
│   ├── index.js
│   ├── not-found.js
│   └── unauthenticated.js
├── middleware/
│   ├── authentication.js
│   ├── error-handler.js
│   └── not-found.js
├── models/
│   ├── Job.js
│   └── User.js
├── routes/
│   ├── auth.js
│   └── jobs.js
├── .env
├── .gitignore
├── app.js
├── package.json
└── swagger.yaml
```

---

## 🏁 Getting Started & Local Setup

Follow these steps to set up and run the project on your local machine.

### Prerequisites

- [Node.js](https://nodejs.org/en/download/) (version 14 or higher)
- An running instance of [MongoDB](https://www.mongodb.com/try/download/community) (you can use a local community edition or a free cluster on MongoDB Atlas).

### Installation Steps

1.  **Clone the repository:**

    ```sh
    git clone [https://github.com/your-username/jobs-api.git](https://github.com/your-username/jobs-api.git)
    ```

2.  **Navigate to the project directory:**

    ```sh
    cd jobs-api
    ```

3.  **Install dependencies:**

    ```sh
    npm install
    ```

4.  **Create an environment variables file (`.env`):**
    Create a file named `.env` in the project's root directory and add the following values:

    ```env
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_super_long_and_random_jwt_secret
    JWT_LIFETIME=30d
    ```

5.  **Run the application:**
    ```sh
    npm start
    ```

Your server should now be running at `http://localhost:3000` (or whichever port you define in your `.env` file).

---

## 🔑 Environment Variables

This project uses environment variables to manage sensitive information:

- `MONGO_URI`: The connection string for your MongoDB database.
- `JWT_SECRET`: A long, random secret key for signing JWTs.
- `JWT_LIFETIME`: The expiration time for tokens (e.g., `30d`, `24h`, `1h`).

---

## 🗺️ API Endpoints Overview

### Authentication (Auth)

- `POST /api/v1/auth/register`: Register a new user
- `POST /api/v1/auth/login`: Log in and receive a token

### Jobs Management (Jobs) - Protected

- `GET /api/v1/jobs`: Get a list of all jobs for the authenticated user
- `POST /api/v1/jobs`: Create a new job
- `GET /api/v1/jobs/:id`: Get information for a specific job
- `PATCH /api/v1/jobs/:id`: Update a job's information
- `DELETE /api/v1/jobs/:id`: Delete a job

---

## 📄 License

This project is distributed under the **MIT License**. See the `LICENSE` file for more information.

---

Built with ❤️ and code.
