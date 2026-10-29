# Student Management System

A web-based Student Management System built using Angular, Node.js, Express.js, and MongoDB. This project is designed to manage student records through a web interface and REST APIs.

## 1. Project Overview

The Student Management System helps manage student information digitally. It provides backend functionality to create, retrieve, update, and delete student records.

The project uses MongoDB to store student data, Express.js to handle API requests, and Node.js to run the backend server.

## 2. Technologies Used

- **Frontend:** Angular
- **Backend:** Node.js
- **Backend Framework:** Express.js
- **Database:** MongoDB
- **ODM:** Mongoose
- **API Architecture:** REST API
- **Middleware:** CORS and Express JSON parsing

## 3. Features

- Add new student records.
- View all students.
- Retrieve a student by ID.
- Update existing student information.
- Delete student records.
- Store student information in MongoDB.
- Handle frontend-to-backend communication through APIs.

## 4. Project Structure

```text
Student-Management-System/
├── backend/
│   ├── app.js
│   ├── database/
│   │   └── db.js
│   ├── model/
│   │   └── Student.js
│   ├── routes/
│   │   └── student.route.js
│   └── package.json
├── src/
│   └── app/
│       └── app-routing.module.ts
├── angular.json
├── app.js
├── package.json
└── README.md
```

## 5. Prerequisites

Install the following tools before running the project:

- Node.js
- npm
- MongoDB Community Server or a MongoDB connection URI
- Angular CLI compatible with the project's Angular version, if the frontend source is complete
- Visual Studio Code or another code editor

## 6. Installation and Setup

### Step 1: Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Student-Management-System
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### Step 2: Install backend dependencies

```bash
cd backend
npm install
```

### Step 3: Configure MongoDB

Open `backend/database/db.js` and verify the database connection.

The current configuration uses:

```text
mongodb://localhost:27017/StudentDetails
```

Make sure MongoDB is running on your computer.

### Step 4: Start the backend server

From the `backend` directory, run:

```bash
node app.js
```

The server uses port `8000` by default, or the port configured through the `PORT` environment variable.

## 7. API Endpoints

The backend provides the following student-management endpoints.

| HTTP Method | Endpoint | Description |
|---|---|---|
| POST | `/api/add-student` | Add a new student |
| GET | `/api/` | Retrieve all students |
| GET | `/api/read-student/:id` | Retrieve a student by ID |
| PUT | `/api/update-student/:id` | Update student information |
| DELETE | `/api/delete-student/:id` | Delete a student |

Use Postman or another REST API client to test these endpoints. For POST and PUT requests, send a JSON body matching the fields defined in `backend/model/Student.js`.

## 8. Frontend Setup

The repository includes Angular configuration files. For a complete Angular application, the development server is typically started using:

```bash
ng serve
```

The frontend development server usually runs at:

```text
http://localhost:4200/
```

**Note:** The supplied project archive appears to be missing standard Angular application files, including `src/main.ts`, `src/index.html`, and component files. The frontend may require additional files and dependencies before it can run successfully.

## 9. Database

MongoDB stores student records in the `StudentDetails` database.

Mongoose defines the student data model and provides methods for interacting with the database.

The database connection can be changed in:

```text
backend/database/db.js
```

For deployment, keep database credentials in environment variables rather than committing them to GitHub.

## 10. Testing

You can test the backend using Postman.

1. Start MongoDB.
2. Start the Node.js backend.
3. Send requests to the API endpoints.
4. Verify that student records are created, retrieved, updated, and deleted correctly.
5. Check server logs if an API request fails.

## 11. Current Limitations

- The supplied archive does not appear to contain the complete Angular frontend.
- The MongoDB connection currently uses a local database URI.
- The project may need additional request validation and consistent error handling.
- Authentication and authorization may be required before production deployment.

## 12. Future Enhancements

- Student login and authentication.
- Admin dashboard.
- Search and filter students.
- Pagination for student records.
- Form validation.
- Improved error handling.
- Responsive user interface.
- Deployment to a cloud platform.

## 13. License

No explicit license was identified in the supplied project files. Add an appropriate `LICENSE` file if you plan to distribute this project publicly.

## 14. Author

**Project:** Student Management System

**Purpose:** To simplify the management of student information through a web application and REST API.
