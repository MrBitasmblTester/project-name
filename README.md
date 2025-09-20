# project-name

## Description

Overview

## Tech Stack
- React
- Node.js

## Requirements
- Users must authenticate via JWT to access protected routes (Hint: Use jsonwebtoken.verify in auth middleware)
- Support creating, reading, updating and deleting tasks via Express routes (Hint: Use express.Router() to organize endpoints)
- Frontend should store JWT and include it in API requests (Hint: Use React Context or localStorage to manage the token)
- Tasks should include a project field and be filterable by project (Hint: Add project property to task object and UI components)
- Display tasks sorted by priority level (Hint: Use Array.sort either in backend or frontend)

## Installation
1. Clone the repository:
   bash
   git clone https://github.com/your-username/project-name.git
   cd project-name
   
2. Back-end setup:
   bash
   cd server
   npm install
   
   Create a `.env` file in the `server` directory with the following variables:
   bash
   JWT_SECRET=your_jwt_secret_key
   PORT=5000
   
3. Front-end setup:
   bash
   cd ../client
   npm install
   

## Usage
1. Start the back-end server:
   bash
   cd server
   npm start
   
2. Start the front-end application:
   bash
   cd ../client
   npm start
   
3. Open your browser and navigate to `http://localhost:3000`.

## Implementation Steps
1. Initialize the back-end with `npm init` and install dependencies (`express`, `jsonwebtoken`, `dotenv`, `cors`).
2. Configure environment variables using `dotenv`.
3. Create an authentication middleware using `jsonwebtoken.verify` to protect routes.
4. Implement `/api/auth/login` endpoint to issue JWT tokens upon valid credentials.
5. Use `express.Router()` to organize CRUD endpoints for tasks under `/api/tasks`.
6. Define the task model with `project` and `priority` fields, and store tasks in-memory or in a database.
7. Apply sorting by `priority` in the GET `/api/tasks` handler.
8. Initialize the front-end with Create React App and install necessary packages.
9. Implement a context or use `localStorage` to manage and include JWT in API requests.
10. Build a login form to authenticate and store the JWT.
11. Create components for listing, filtering by project, and sorting tasks by priority.
12. Develop forms for creating and updating tasks and connect them to the back-end API.

## API Endpoints
- POST `/api/auth/login` - Authenticate user and receive JWT.
- GET `/api/tasks` - Retrieve all tasks (protected).
- POST `/api/tasks` - Create a new task (protected).
- GET `/api/tasks/:id` - Retrieve a task by ID (protected).
- PUT `/api/tasks/:id` - Update a task by ID (protected).
- DELETE `/api/tasks/:id` - Delete a task by ID (protected).