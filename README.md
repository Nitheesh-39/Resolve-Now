# complaint-registry
Resolve-Now

Resolve-Now is a full-stack complaint/grievance management platform built on the MERN stack. Users can register, file complaints with location and issue details, and track their status through resolution — while admins can review, manage, and update complaint status.

Features
🔐 User registration & authentication (name, email, password, phone, user type)
📝 Complaint filing with detailed location info (address, city, state, pincode)
📊 Complaint status tracking (open, in-progress, resolved, etc.)
🔗 Complaints linked to the users who filed them via MongoDB references
🖥️ Separate frontend and backend codebases for clean separation of concerns
Tech Stack

Backend

Node.js
Express.js
MongoDB with Mongoose (schema-based modeling)

Frontend

React.js (see /frontend)
Project Structure
Resolve-Now/
├── backend/          # Express API, Mongoose schemas, routes, controllers
├── frontend/         # React client application
├── package.json
└── README.md
Data Models

User

Field	Type	Required
name	String	✅
email	String	✅
password	String	✅
phone	Number	✅
userType	String	✅

Complaint

Field	Type	Required
userId	ObjectId (ref: User)	✅
name	String	✅
address	String	✅
city	String	✅
state	String	✅
pincode	Number	✅
comment	String	✅
status	String	✅
Getting Started
Prerequisites
Node.js (v16+ recommended)
MongoDB (local instance or Atlas connection string)
