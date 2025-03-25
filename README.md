# Contacts Manager API

This is a **RESTful API** built with **Node.js, Express.js, and MongoDB** for managing contacts. It provides user authentication and CRUD operations for contacts.

## Features
- User authentication (Register, Login, JWT-based authentication)
- Secure routes with token validation
- CRUD operations for managing contacts
- Error handling middleware

## Technologies Used
- **Node.js**
- **Express.js**
- **MongoDB & Mongoose**
- **JWT (JSON Web Token)**
- **Bcrypt.js** (password hashing)
- **dotenv** (environment variables)

## Installation

1. **Clone the repository**
   ```sh
   git clone https://github.com/erftube/contacts-manager-api.git
   cd contacts-backend-api
   ```

2. **Install dependencies**
   ```sh
   npm install
   ```

3. **Create a `.env` file** and add the following:
   ```sh
   PORT=5001
   DB_STRING= YOUR_DB_CONNECTION_STRING
   ACCESS_TOKEN_SECRET= YOUR_TOKEN_SECRET
   ```

4. **Run the server**
   ```sh
   npm run dev   # Starts the server in development mode
   npm start     # Starts the server in production mode
   ```

## API Endpoints

### **User Routes**
| Method | Endpoint          | Description          | Access   |
|--------|------------------|----------------------|----------|
| POST   | `/api/users/register` | Register a new user | Public   |
| POST   | `/api/users/login`    | Login user & get token | Public   |
| GET    | `/api/users/current`  | Get current user info | Private  |

### **Contact Routes** (Requires Authentication)
| Method | Endpoint          | Description          |
|--------|------------------|----------------------|
| GET    | `/api/contacts`     | Get all contacts for the user |
| POST   | `/api/contacts`     | Create a new contact |
| GET    | `/api/contacts/:id` | Get a single contact |
| PUT    | `/api/contacts/:id` | Update a contact |
| DELETE | `/api/contacts/:id` | Delete a contact |

## Folder Structure
```
express/
│── config/
│   ├── dbConnection.js
│── controllers/
│   ├── contactController.js
│   ├── userControllers.js
│── middleware/
│   ├── errorHandler.js
│   ├── validateTokenHandler.js
│── models/
│   ├── contactModel.js
│   ├── userModel.js
│── routes/
│   ├── contactRoutes.js
│   ├── userRoutes.js
│── .env
│── constants.js
│── package.json
│── server.js
```

## License
This project is licensed under the **MIT License**.

## Author
**Erftube**

Feel free to contribute and improve this project!
