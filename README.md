# KCET System Documentation

## Project Overview
The KCET System is designed to streamline the process of conducting and evaluating entrance exams for prospective engineering and medical students in Karnataka. It focuses on providing a transparent, efficient, and user-friendly platform for students and administrators alike.

## Technology Stack
- **Frontend**: ReactJS
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Authentication**: JWT
- **Hosting**: AWS

## Database Schema
- **Users**: 
  - `userId`: String (Primary Key)
  - `name`: String
  - `email`: String
  - `password`: String
  - `role`: String (Admin/User)

- **Exams**: 
  - `examId`: String (Primary Key)
  - `title`: String
  - `date`: Date
  - `duration`: Number

- **Results**: 
  - `resultId`: String (Primary Key)
  - `userId`: String (Foreign Key)
  - `examId`: String (Foreign Key)
  - `score`: Number
  - `status`: String (Pass/Fail)

## Setup Instructions
1. Clone the repository: `git clone https://github.com/Chandubr/common-entrance-exam-clone.git`
2. Navigate to the project directory: `cd common-entrance-exam-clone`
3. Install dependencies: `npm install`
4. Set up environment variables in a `.env` file:
   - `MONGODB_URI=<your_mongodb_uri>`
   - `JWT_SECRET=<your_jwt_secret>`
5. Start the application: `npm start`

## API Documentation
- **GET /api/exams** - Retrieve all exams.
- **POST /api/exams** - Create a new exam.
- **GET /api/results/:userId** - Retrieve results for a user.

## Troubleshooting Guide
- **Common Issues**:
  - Ensure that MongoDB is running when starting the server.
  - Verify that environment variables are correctly set.

## Best Practices
- Regularly update dependencies to avoid security vulnerabilities.
- Implement error handling for all API endpoints.
- Write unit tests for critical functionalities.