# 👤 User Management Backend API

This is a **Node.js + Express.js + MongoDB** based RESTful API that allows full CRUD operations (Create, Read, Update, Delete) for managing users. The application is structured using the **MVC architecture** for clean and maintainable code.

---

## 📁 Project Structure
/MONGO-EXPRESS
├── config/ # MongoDB connection setup
├── controllers/ # Logic for user operations
├── models/ # Mongoose schema and model
├── routes/ # Express routes
├── views/ # Response formatters (renderers)
├── .env # Environment variables (hidden from Git)
├── index.js # Main app entry point


---

## 🚀 Features

- 🔁 Full REST API (GET, POST, PUT, DELETE)
- ✅ Validation using Mongoose
- 🔒 Custom error handling
- 🧪 Health check route
- 🗂 Organized using MVC pattern
- 📦 Connected to MongoDB for persistent storage

---

## 🛢️ Database Usage (MongoDB)

This project uses **MongoDB** as its database.

- Connection is made using `mongoose` inside `/config/db.js` file.
- Connection string comes from `.env` file:

- The `User` model (in `/models/userModel.js`) defines the schema for storing:
- Name (String)
- Email (String, Unique)
- Age (Number)

### CRUD operations are performed like this:

| Operation | Code Snippet                              |
|-----------|--------------------------------------------|
| Create    | `User.create(req.body)`                   |
| Read      | `User.find()` / `User.findById(id)`       |
| Update    | `User.findByIdAndUpdate(id, data)`        |
| Delete    | `User.findByIdAndDelete(id)`              |

> All data is stored in a MongoDB collection named `users`.

---

## 📡 API Endpoints

GET /health
Response: { "status": "OK" }

| Method | Endpoint     | Description          |
| ------ | ------------ | -------------------- |
| GET    | `/users`     | Get all users        |
| GET    | `/users/:id` | Get user by ID       |
| POST   | `/users`     | Create a new user    |
| PUT    | `/users/:id` | Update existing user |
| DELETE | `/users/:id` | Delete a user        |

##📘 Sample JSON for Creating User

{
  "name": "Muqaddas Fatima",
  "email": "muqaddas@example.com",
  "age": 22
}

##💻 Tech Stack

  Node.js
  Express.js
  MongoDB + Mongoose
  dotenv
  MVC Architecture
