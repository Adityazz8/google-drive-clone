Google Drive Clone – Backend System

A scalable file storage backend inspired by Google Drive, built using Node.js, Express, and EJS, focusing on clean architecture, modular routing, and efficient file handling.
This project demonstrates real-world backend engineering skills including file uploads, server-side rendering, middleware usage, and structured project design.

This project is not just a CRUD app.
It showcases :-
-Design a production-style backend architecture
-Handle file uploads & storage safely
-Build modular, readable, and maintainable code
-Work with Node.js ecosystem tools used in real companies
-The goal was to understand how cloud storage platforms work at a backend level, not just replicate UI.

# Core Features

- File upload using server-side middleware
- Secure file storage on disk
- File listing & management
- Server-side rendered views using EJS
- Modular routing and separation of concerns
- Clean project structure suitable for scaling

# System Architecture

Client (Browser)
   ↓
EJS Views (Server-Rendered UI)
   ↓
Express Routes
   ↓
Controllers / Middleware
   ↓
File System (Uploads Directory)


This architecture ensures:
Clear responsibility separation
Easy debugging and maintenance
Readiness for database & auth integration

📁 Project Structure 

google-drive-clone/
│
├── config/          # Application & environment configuration
│
├── models/          # Data models (file metadata abstraction)
│
├── routes/          # Express route handlers (upload, download, listing)
│
├── uploads/         # Physical file storage location
│
├── views/           # EJS templates (server-rendered UI)
│
├── app.js           # Main application entry point
│
├── package.json     # Dependencies & scripts
└── README.md

🔑 Key Files Explained

app.js
Initializes Express server
Registers middleware
Configures view engine
Connects routes
Starts HTTP server
This file acts as the application backbone.

📦 Tech Stack

Node.js -Backend runtime
Express.js - Web server & routing
EJS	Server - side templating
Multer - File upload handling
File System (FS) - Storage engine
Nodemon -	Development productivity

⚙️ How File Upload Works

- User submits file via HTML form
- Request hits Express route
- Multer middleware:
    - Validates request
    - Renames file safely
    - Stores file in /uploads
- Server responds with updated file list
This mimics cloud storage ingestion pipelines at a basic level.

🚀 How to Run Locally

npm install
npm start

Server runs on:
http://localhost:3000

🔒 Security Considerations Implemented

Controlled upload directory
Middleware-based file handling
No direct client filesystem access
Server-side rendering (reduced XSS surface)

🧪 Engineering Decisions

Why EJS instead of React?
→ To focus on backend logic and server-side rendering fundamentals.

Why filesystem storage?
→ To understand low-level storage handling before abstracting to cloud providers.

Why modular routing?
→ Enables easy scaling into microservices or REST APIs.

📈 Future Enhancements

🔐 User authentication & authorization
☁️ Cloud storage (AWS S3 / GCP)
🗃️ Database integration (MongoDB)
📂 Folder hierarchy
🔄 File sharing & permissions
📊 Upload analytics

💼 Skills Demonstrated 

✔ Backend system design
✔ Node.js & Express proficiency
✔ Middleware & file handling
✔ Clean folder architecture
✔ Real-world project structure
✔ Readable & maintainable code

👨‍💻 Author

Aditya Borse
🔗 GitHub: https://github.com/Adityazz8
