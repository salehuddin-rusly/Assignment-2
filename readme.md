# TaskMaster Pro API

This is a REST API for a task management app built with Express, Sequelize, and Postgres.

## Requirements
* Node.js installed
* PostgreSQL installed

## How to install
1. Clone this repo to your computer.
2. Open terminal and run: npm install

## Database setup
1. Open Postgres and create a database named: `taskmaster_db`
2. Create a `.env` file in the main folder and put this inside:

```text
PORT=3000
DB_NAME=taskmaster_db
DB_USER=your_username
DB_PASS=your_password
DB_HOST=localhost
DB_DIALECT=postgres
```

3. The tables will create themselves when you run the app.

## How to run
* For development: npm run dev
* For production: npm start

## API Routes

### Users
* **POST /users** - Create new user (needs name, email)
* **GET /users** - Get all users
* **GET /users/:id** - Get user by ID
* **DELETE /users/:id** - Delete user and their tasks

### Tasks
* **POST /tasks** - Create a task (needs title, description, dueDate, userId)
* **GET /tasks** - Get all tasks and the user data
* **GET /tasks/:id** - Get a task by ID
* **PUT /tasks/:id** - Update task details
* **DELETE /tasks/:id** - Delete task