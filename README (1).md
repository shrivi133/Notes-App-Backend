# Notes App Backend - REST API

A secure Node.js & Express REST API for a notes-taking application using MongoDB and JSON Web Token (JWT) authentication.

## 🚀 Features
- **User Authentication:** Registration and login endpoints with password hashing using `bcryptjs`.
- **JWT Protection:** Protected routes verified with bearer token authorization middleware.
- **Full CRUD Operations:** Authenticated users can create, read, update, and delete their own notes.
- **Data Isolation:** Each note is securely linked to the specific authenticated user.

## 🛠️ Tech Stack
- **Node.js** & **Express.js**
- **MongoDB** & **Mongoose**
- **JSON Web Tokens (JWT)**
- **Bcrypt.js**

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - Create a new user account
- `POST /api/auth/login` - Authenticate user and return JWT token

### Notes (Requires `Authorization: Bearer <token>`)
- `POST /api/notes` - Create a new note
- `GET /api/notes` - Retrieve all notes for the authenticated user
- `PUT /api/notes/:id` - Update an existing note
- `DELETE /api/notes/:id` - Delete a note

## 💻 Local Setup
1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file based on `.env.example`:
   ```env
   PORT=5000
   MONGO_URI=mongodb://127.0.0.1:27017/notes_db
   JWT_SECRET=your_jwt_secret_key_here
   ```
4. Start the server:
   ```bash
   npm start
   ```
