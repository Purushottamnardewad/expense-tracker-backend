# Expense Tracker – Backend

This is the backend for the Expense Tracker application.  
It is built using Node.js, Express, and MongoDB and provides APIs for authentication and expense management.

---

## Features

- User signup and login
- Password hashing
- JWT-based authentication
- Add, view, update, and delete expenses
- Each user can only access their own expenses

---

## Tech Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcrypt
- dotenv

---
---

## Setup Instructions

### 1. Install dependencies

```bash
npm install
```
### 2. Environment variables

Create a .env file using .env.example:
```bash
PORT=5001
MONGODB_URI=mongodb://localhost:27017/expense-tracker
JWT_SECRET=your_secret_key
```
### 3. Start the server
```bash
npm run dev
```

Backend will run on:
```bash
http://localhost:5001
```

## API Endpoints

### Authentication
1. POST /api/auth/signup – Register user
2. POST /api/auth/login – Login user

## Expenses (Protected routes)
1. GET /api/expenses – Get all expenses
2. POST /api/expenses – Add new expense
3. PUT /api/expenses/:id – Update expense
4. DELETE /api/expenses/:id – Delete expense

All protected routes require a JWT token in headers:
```bash
Authorization: Bearer <token>
```
# Note
1. Expenses are linked to the logged-in user
2. JWT middleware protects all expense routes
3. API response format is aligned with frontend expectations
