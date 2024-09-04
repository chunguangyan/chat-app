# chat-app
Angular & Node.js Chat System - Phase 1

1. Project Overview

This project is the first phase of a chat system built using Angular for the frontend and Node.js for the backend. The first phase includes:

User Authentication: A basic login system that verifies users.
Group and Channel Management: Super Admins can create groups, add users to groups, and create channels within groups. Only users added to specific channels can access those channels.
Data Storage: User, group, and channel data are stored in a local JSON file during Phase 1.
REST API: Frontend communicates with the backend via RESTful API calls.
The system uses local storage in the browser to store the logged-in user's information.

2. Installation Guide

2.1 Clone the Project
bash
Copy code
git clone https://github.com/your-repo/chat-app.git
2.2 Backend Installation (Node.js)
Navigate to the server directory:
bash
Copy code
cd server
Install the required dependencies:
bash
Copy code
npm install
Start the Node.js server:
bash
Copy code
node app.js
The server will run at http://localhost:3000.
2.3 Frontend Installation (Angular)
Navigate to the chat-app directory:
bash
Copy code
cd chat-app
Install the required dependencies:
bash
Copy code
npm install
Start the Angular development server:
bash
Copy code
ng serve
The frontend will be available at http://localhost:4200.
3. Usage

3.1 User Login
Visit http://localhost:4200/login.
Use the following credentials to log in:
Username: admin
Password: admin
After successful login, the system stores the logged-in user's information in the browser's local storage.
3.2 Group and Channel Management
After login, Super Admins can create new groups and add users to the groups.
Group Admins can create channels within their groups, and only users who are explicitly added to a channel can view its content.
4. Project Structure

bash
Copy code
chat-app/
├── src/
│   ├── app/
│   │   ├── login.component.ts      # Login component
│   │   ├── services/
│   │   │   └── auth.service.ts     # Service for handling login API requests
│   ├── assets/                     # Static assets
├── package.json                    # Frontend dependencies and project information
└── angular.json                    # Angular project configuration

server/
├── app.js                          # Node.js server entry point
├── routes/
│   └── userRoutes.js               # User login API routes
├── controllers/
│   └── userController.js           # Controller handling user login logic
├── data/
│   └── data.json                   # Local data storage for users, groups, and channels
├── package.json                    # Backend dependencies and project information
