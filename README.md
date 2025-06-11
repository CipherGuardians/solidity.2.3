# Homework Task Management System

## Description

A simple application for managing homework and personal tasks.  
This project was created as part of university coursework to demonstrate practical skills in Node.js, the MVC pattern, and Server-Side Rendering (SSR).

---

## Features

- Add new homework tasks with title, description, and deadline (date & time)
- Edit existing tasks
- Mark tasks as completed
- Delete tasks
- **Overdue tasks are highlighted** in the interface
- **Sort/filter tasks by deadline or by completion status** ("All tasks", "Only active", "Only completed")
- Simple and clear web interface (minimum styling for readability)

---

## Stack & External Libraries

- **Node.js** — server-side JavaScript
- **Express** — web framework
- **MongoDB** — database (native `mongodb` driver)
- **EJS** — templates/views (SSR)
- **dotenv** — for environment variables
- **body-parser** — for form data
- **method-override** — for supporting PUT/DELETE via POST
- **nodemon** (dev only) — auto-reload during development

---

## Project Structure

homework-mvc/
│
├── config/
│   └── db.js             # MongoDB connection
│
├── controllers/
│   └── taskController.js # Task business logic
│
├── models/
│   └── Task.js           # Task DAO (database access functions)
│
├── routes/
│   └── taskRoutes.js     # All app routes
│
├── views/
│   ├── layout.ejs        # Main layout
│   ├── index.ejs         # Task list (main page)
│   ├── add.ejs           # Add task form
│   └── edit.ejs          # Edit task form
│
├── public/
│   └── style.css         # All CSS styles
│
├── .env                  # Environment variables (MongoDB URI etc.)
├── .gitignore
├── app.js                # App entry point
├── package.json
└── README.md

## How to Run

1. **Clone the repository**
   git clone https://github.com/yourusername/homework-mvc.git
   cd homework-mvc

2. **Install dependencies**
   npm install

3. **Set up environment variables**
   Create a .env file in the root directory:

   PORT=3000
   MONGO_URI=mongodb://localhost:27017/homeworkdb

4. **Run MongoDB**
   Make sure your MongoDB server is running (by default on mongodb://localhost:27017).

5. **Start the server**
   npm start

   For development with auto-reload:
   npm run dev

6. **Open in browser:**
   http://localhost:3000

---

## Functional Requirements

- **Add a task:** with title, description, and deadline.
- **Edit a task:** update title, description, deadline.
- **Mark as done:** toggle task as completed.
- **Delete a task:** remove from database.
- **Highlight overdue tasks:** any task whose deadline is in the past and not completed is visually marked.
- **Sort/filter tasks:**
  - By deadline (default: closest at the top)
  - By status: "Only active" (not done), "Only completed" (done), "All tasks" (default).

---

## Example Input

Add task form:
- **Title:** Math homework
- **Description:** Solve problems 5–10 on page 37.
- **Deadline:** 2024-06-13 20:00

Mark as done: Click "Done" next to task.

---

## About MVC Implementation

- **Model:** models/Task.js (DAO for MongoDB collection)
- **View:** all .ejs templates in /views/
- **Controller:** controllers/taskController.js
- **Router:** routes/taskRoutes.js
- **Database connection:** config/db.js
- **Static assets:** /public/style.css

---

## License

For educational/university use only.
