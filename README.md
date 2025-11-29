# QuickChat

A modern, real-time chat application built with React, Express, and Socket.io. QuickChat enables users to communicate instantly with real-time messaging, user authentication, and profile management.

## 🌟 Features

- **Real-time Messaging**: Instant message delivery using Socket.io
- **User Authentication**: Secure login and registration with JWT
- **User Profiles**: View and manage user profiles with profile pictures
- **Cloud Image Storage**: Images stored securely with Cloudinary
- **Responsive Design**: Mobile-friendly UI built with Tailwind CSS
- **Message Persistence**: Chat history stored in MongoDB
- **Password Security**: Encrypted passwords using bcryptjs

## 🏗️ Project Structure

```
QuickChat/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # React components (ChatContainer, Sidebar, RightSidebar)
│   │   ├── pages/         # Pages (HomePage, LoginPage, ProfilePage)
│   │   ├── context/       # React Context (AuthContext, ChatContext)
│   │   ├── lib/           # Utility functions
│   │   ├── assets/        # Static assets
│   │   └── App.jsx        # Main app component
│   ├── vite.config.js     # Vite configuration
│   └── package.json       # Client dependencies
│
└── server/                # Express backend
    ├── controllers/       # Route controllers (userController, messageController)
    ├── models/           # MongoDB schemas (User, Message)
    ├── routes/           # API routes (userRoutes, messageRoutes)
    ├── middleware/       # Express middleware (auth)
    ├── lib/              # Database and utility functions
    ├── server.js         # Express server setup
    └── package.json      # Server dependencies
```

## 🚀 Tech Stack

### Frontend
- **React** 19.2.0 - UI library
- **Vite** 7.2.2 - Build tool and dev server
- **Tailwind CSS** 4.1.17 - Utility-first CSS framework
- **React Router DOM** 7.9.6 - Client-side routing
- **Socket.io Client** 4.8.1 - Real-time communication
- **Axios** 1.13.2 - HTTP client
- **React Hot Toast** 2.6.0 - Toast notifications

### Backend
- **Express** 5.1.0 - Web framework
- **MongoDB & Mongoose** 8.19.4 - Database and ODM
- **Socket.io** 4.8.1 - Real-time bidirectional communication
- **JWT** 9.0.2 - Token-based authentication
- **bcryptjs** 3.0.3 - Password hashing
- **Cloudinary** 2.8.0 - Image hosting service
- **CORS** 2.8.5 - Cross-origin resource sharing
- **dotenv** 17.2.3 - Environment variables

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm or yarn
- MongoDB instance (local or cloud)
- Cloudinary account (for image uploads)

## 🔧 Installation

### 1. Clone the repository
```bash
git clone https://github.com/ash2573/QuickChat.git
cd QuickChat
```

### 2. Setup Backend

Navigate to the server directory and install dependencies:
```bash
cd server
npm install
```

Create a `.env` file in the server directory with the following variables:
```env
PORT=5000
NODE_ENV=development
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

### 3. Setup Frontend

Navigate to the client directory and install dependencies:
```bash
cd ../client
npm install
```

Create a `.env` file in the client directory:
```env
VITE_API_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000
```

## ▶️ Running the Application

### Backend (from server directory)
```bash
npm run server    # Development mode with nodemon
npm start         # Production mode
```

### Frontend (from client directory)
```bash
npm run dev       # Development mode
npm run build     # Build for production
npm run preview   # Preview production build
```

The frontend will typically run on `http://localhost:5173` and the backend on `http://localhost:5000`.

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `POST /api/auth/logout` - User logout

### Users
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user profile

### Messages
- `GET /api/messages/:userId` - Get messages with a user
- `POST /api/messages` - Send a message
- `DELETE /api/messages/:id` - Delete a message

## 🔐 Environment Variables

### Server `.env`
- `PORT` - Server port (default: 5000)
- `NODE_ENV` - Environment (development/production)
- `MONGODB_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `CLOUDINARY_CLOUD_NAME` - Cloudinary cloud name
- `CLOUDINARY_API_KEY` - Cloudinary API key
- `CLOUDINARY_API_SECRET` - Cloudinary API secret

### Client `.env`
- `VITE_API_URL` - Backend API URL
- `VITE_SOCKET_URL` - Socket.io server URL

## 📁 Key Files

### Client
- `context/AuthContext.jsx` - Authentication state management
- `context/ChatContext.jsx` - Chat state management
- `components/ChatContainer.jsx` - Main chat interface
- `components/Sidebar.jsx` - User list and navigation
- `pages/HomePage.jsx` - Main chat page
- `pages/LoginPage.jsx` - Authentication page
- `pages/ProfilePage.jsx` - User profile management

### Server
- `models/User.js` - User schema and model
- `models/Message.js` - Message schema and model
- `controllers/userController.js` - User logic
- `controllers/messageController.js` - Message logic
- `middleware/auth.js` - JWT authentication middleware
- `lib/db.js` - MongoDB connection
- `lib/cloudinary.js` - Cloudinary configuration

## 🧪 Testing

### Linting
```bash
cd client
npm run lint      # Run ESLint
```

## 🚀 Deployment

### Vercel Deployment

Both client and server include `vercel.json` configuration files for easy deployment to Vercel.

**Frontend:**
1. Push code to GitHub
2. Connect repository to Vercel
3. Set environment variables in Vercel dashboard
4. Deploy

**Backend:**
1. Deploy Express server to Vercel
2. Update `VITE_API_URL` in client to point to deployed backend
3. Re-deploy frontend with updated API URL

## 📝 License

This project is licensed under the ISC License.

## 👨‍💻 Author

- **ash2573**

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Support

For issues or questions, please open an issue on the GitHub repository.

---

**Last Updated**: November 2025
