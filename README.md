# CloudManager

[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-green)](https://www.mongodb.com/atlas)

A full-stack CloudManager built with Node.js, Express, MongoDB, and Cloudinary. Upload, manage, and share your files securely with user authentication and cloud storage.

## ✨ Features

- 🔐 **User Authentication**: Secure registration and login with JWT tokens
- 📁 **File Upload**: Upload files of various formats to Cloudinary storage
- 📋 **File Management**: View, download, and delete your uploaded files
- 🔒 **Secure Access**: Protected routes with authentication middleware
- 🎨 **Modern UI**: Clean and responsive interface using EJS templates
- ☁️ **Cloud Storage**: Reliable file storage with Cloudinary CDN
- 🗄️ **Database Integration**: MongoDB Atlas for user and file metadata
- 📱 **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB Atlas** - NoSQL database
- **Mongoose** - ODM for MongoDB
- **JWT** - JSON Web Tokens for authentication
- **bcrypt** - Password hashing

### Frontend
- **EJS** - Templating engine
- **CSS** - Styling (custom)
- **JavaScript** - Client-side interactions

### Storage & Services
- **Cloudinary** - Cloud storage and CDN
- **Multer** - File upload middleware

## 📋 Prerequisites

Before running this application, make sure you have:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB Atlas](https://www.mongodb.com/atlas) account (free tier available)
- [Cloudinary](https://cloudinary.com/) account (free tier available)

## 📖 Usage

### User Registration
1. Visit `http://localhost:3000/user/register`
2. Fill in your details (username, email, password)
3. Click "Register"

### User Login
1. Visit `http://localhost:3000/user/login`
2. Enter your credentials
3. Click "Login" to access your dashboard

### File Operations
- **Upload**: Select a file and click "Upload File"
- **View**: See all your uploaded files in the "Your Files" section
- **Download**: Click on any file link to download
- **Delete**: Use the delete button next to each file

## 🏗️ Project Structure

```
google-drive-clone/
├── config/
│   ├── config.js          # Cloudinary configuration
│   └── db.js              # MongoDB connection
├── middleware/
│   └── ...                # Custom middleware
├── models/
│   ├── file.model.js      # File schema
│   └── user.model.js      # User schema
├── routes/
│   ├── index.routes.js    # Main application routes
│   └── user.routes.js     # User authentication routes
├── views/
│   ├── home.ejs           # Dashboard/home page
│   ├── index.ejs          # Landing page
│   ├── login.ejs          # Login form
│   └── register.ejs       # Registration form
├── uploads/               # Temporary upload directory
├── app.js                 # Main application file
├── package.json           # Dependencies and scripts
├── .env.example           # Environment variables template
└── README.md             # Project documentation
```

## 🔌 API Endpoints

### Authentication Routes
- `GET /user/register` - Registration page
- `POST /user/register` - Register new user
- `GET /user/login` - Login page
- `POST /user/login` - Authenticate user
- `POST /user/logout` - Logout user

### File Management Routes
- `GET /home` - User dashboard (authenticated)
- `POST /upload` - Upload file (authenticated)
- `GET /files` - Get user's files (authenticated)
- `DELETE /files/:id` - Delete specific file (authenticated)

### Utility Routes
- `GET /` - Root route (redirects to login or home)
- `GET /login` - Redirect to login page
- `GET /register` - Redirect to registration page

### Code Quality

- Uses ESLint for code linting (configure as needed)
- Follows standard Node.js project structure
- Implements proper error handling and validation

## 🐛 Troubleshooting

### Common Issues

**"MongoDB connection error"**
- Verify your `MONGO_URI` in `.env`
- Check IP whitelist in MongoDB Atlas
- Ensure network connectivity

**"File upload failed"**
- Validate Cloudinary credentials
- Check file size limits (100MB for free tier)
- Verify internet connection

**"Authentication failed"**
- Clear browser cookies
- Check JWT_SECRET configuration
- Verify user credentials

For detailed troubleshooting steps, see [SETUP_GUIDE.md](SETUP_GUIDE.md).

## 📊 File Limits (Free Tier)

| Service | Storage | Bandwidth | File Size |
|---------|---------|-----------|-----------|
| MongoDB Atlas | 512 MB | - | - |
| Cloudinary | 25 GB | 25 GB/month | 100 MB |


## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.
