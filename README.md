# CivicWatch 🏛️

A comprehensive civic issue reporting system that enables citizens to report community problems and allows administrators to manage and track resolution progress in real-time.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## 🌟 Overview

CivicWatch is a full-stack web application designed to bridge the gap between citizens and local government by providing an intuitive platform for reporting and managing community issues. Citizens can easily submit reports with photos and location details, while administrators can efficiently track, categorize, and resolve these issues.

## ✨ Features

### For Citizens
- **Easy Report Submission**: Submit issues with descriptions, photos, and location data
- **Real-time Tracking**: Monitor report status from submission to resolution
- **Personal Dashboard**: View all submitted reports and their current status
- **Interactive Map**: Visualize community issues on an interactive map
- **Notifications**: Receive updates on report progress
- **Mobile-Friendly**: Responsive design for all devices

### For Administrators
- **Centralized Dashboard**: Overview of all reports with key metrics
- **Advanced Filtering**: Filter reports by status, category, priority, and department
- **Status Management**: Update report statuses and assign to departments
- **Analytics**: Comprehensive analytics with charts and performance insights
- **Department Assignment**: Route reports to appropriate departments
- **Bulk Operations**: Efficiently manage multiple reports

### General Features
- **Secure Authentication**: JWT-based authentication for users and admins
- **Role-based Access**: Different interfaces for citizens and administrators
- **File Upload**: Support for image attachments with reports
- **Real-time Updates**: Live status updates and notifications
- **Data Visualization**: Charts and graphs for analytics

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern UI library
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Beautiful icons
- **Recharts** - Data visualization library

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - Authentication tokens
- **Multer** - File upload handling
- **bcrypt** - Password hashing

### Development Tools
- **Concurrently** - Run multiple commands
- **Nodemon** - Development server auto-restart
- **CORS** - Cross-origin resource sharing
- **dotenv** - Environment variable management

## 📁 Project Structure

```
CivicWatch/
├── client/                 # React frontend application
│   ├── public/            # Static files
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── context/       # React context providers
│   │   ├── pages/         # Application pages/routes
│   │   ├── data/          # Static data files
│   │   └── App.jsx        # Main application component
│   ├── .env               # Environment variables
│   └── package.json       # Frontend dependencies
├── server/                # Node.js backend application
│   ├── src/
│   │   ├── middleware/    # Express middleware
│   │   ├── models/        # Mongoose data models
│   │   ├── routes/        # API route handlers
│   │   └── index.js       # Server entry point
│   ├── uploads/           # File upload storage
│   ├── .env               # Server environment variables
│   └── package.json       # Backend dependencies
└── package.json           # Root package configuration
```

## 🚀 Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- Git

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/gopikiran22001/CivicWatch.git
   cd CivicWatch
   ```

2. **Install all dependencies**
   ```bash
   npm run install-all
   ```

3. **Set up environment variables**
   
   **Server (.env in /server directory):**
   ```env
   PORT=5000
   NODE_ENV=development
   MONGODB_URI=mongodb://localhost:27017/civicwatch
   JWT_SECRET=your_jwt_secret_key_here
   JWT_EXPIRE=7d
   CLIENT_URL=http://localhost:3000
   MAX_FILE_SIZE=5242880
   ```

   **Client (.env in /client directory):**
   ```env
   REACT_APP_API_BASE_URL=http://localhost:5000/api
   ```

4. **Start the application**
   ```bash
   npm start
   ```

   This will start both the backend server (port 5000) and frontend client (port 3000).

### Individual Setup

**Backend Only:**
```bash
cd server
npm install
npm run dev
```

**Frontend Only:**
```bash
cd client
npm install
npm start
```

## ⚙️ Configuration

### Database Setup

1. **Local MongoDB:**
   - Install MongoDB locally
   - Start MongoDB service
   - Update `MONGODB_URI` in server/.env

2. **MongoDB Atlas (Cloud):**
   - Create a MongoDB Atlas account
   - Create a new cluster
   - Get connection string and update `MONGODB_URI`

### Seeding Data

**Seed Categories:**
```bash
cd server
npm run seed
```

**Create Admin User:**
```bash
cd server
npm run add_admin
```

**Check Existing Admins:**
```bash
cd server
npm run check-admins
```

## 📖 Usage

### For Citizens

1. **Register/Login**: Create an account or sign in
2. **Submit Report**: Click "Report an Issue" and fill out the form
3. **Track Progress**: View reports in "My Reports" section
4. **View Map**: See community issues on the interactive map

### For Administrators

1. **Admin Login**: Use admin credentials to access admin panel
2. **Dashboard**: View overview of all reports and statistics
3. **Manage Reports**: Update statuses, assign departments
4. **Analytics**: View detailed analytics and trends

### API Endpoints

**Authentication:**
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/admin-auth/login` - Admin login

**Reports:**
- `GET /api/reports` - Get all reports
- `POST /api/reports` - Create new report
- `GET /api/reports/my-reports` - Get user's reports
- `PUT /api/reports/:id` - Update report status

**Categories:**
- `GET /api/categories` - Get all categories

## 🔧 Development

### Available Scripts

**Root Directory:**
- `npm run install-all` - Install all dependencies
- `npm start` - Start both client and server
- `npm run server` - Start server only
- `npm run client` - Start client only

**Server Directory:**
- `npm run dev` - Start development server
- `npm run seed` - Seed database with categories
- `npm run add_admin` - Create admin user

**Client Directory:**
- `npm start` - Start development server
- `npm run build` - Build for production
- `npm test` - Run tests

### Environment Variables

**Required Server Variables:**
- `MONGODB_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `PORT` - Server port (default: 5000)

**Required Client Variables:**
- `REACT_APP_API_BASE_URL` - Backend API URL

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the ISC License.

## 👥 Authors

**Bug_Slayers Team**
- GitHub: [@gopikiran22001](https://github.com/gopikiran22001)

## 🐛 Issues

Report bugs and request features at: [GitHub Issues](https://github.com/gopikiran22001/CivicWatch/issues)

## 🌐 Live Demo

- **Frontend**: [CivicWatch Client](https://neon-kulfi-0f24e3.netlify.app)
- **Backend API**: [CivicWatch API](https://civicwatch-mrg9.onrender.com)

---

**Made with ❤️ for better communities**
