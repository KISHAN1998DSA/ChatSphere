# 💬 Chat-Sphere

A modern, full-stack real-time chat application built with the MERN stack, featuring authentication, one-to-one messaging, group chats, and real-time communication powered by Socket.IO.

![MERN Stack](https://img.shields.io/badge/Stack-MERN-green)
![Socket.IO](https://img.shields.io/badge/Real--Time-Socket.IO-blue)
![Chakra UI](https://img.shields.io/badge/UI-Chakra%20UI-teal)

## ✨ Features

- 🔐 **JWT Authentication** - Secure user registration and login
- 💬 **Real-Time Messaging** - Instant message delivery with Socket.IO
- 👥 **Group Chats** - Create and manage group conversations
- 🔍 **User Search** - Find and connect with other users
- 🎨 **Modern UI** - Beautiful, responsive interface with Chakra UI
- 🌙 **Dark Mode** - Eye-friendly dark theme support
- 📱 **Responsive Design** - Works seamlessly on all devices
- ⌨️ **Typing Indicators** - See when others are typing
- 🔔 **Notifications** - Get notified of new messages

## 🛠 Tech Stack

### Frontend
- **React** - UI library
- **Chakra UI** - Component library
- **Socket.IO Client** - Real-time communication
- **Axios** - HTTP client
- **React Router** - Navigation

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **Socket.IO** - Real-time engine
- **JWT** - Authentication
- **bcrypt** - Password hashing

## 📁 Project Structure

```
chat-sphere/
├── backend/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── userController.js
│   │   ├── chatController.js
│   │   └── messageController.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorMiddleware.js
│   ├── models/
│   │   ├── userModel.js
│   │   ├── chatModel.js
│   │   └── messageModel.js
│   ├── routes/
│   │   ├── userRoutes.js
│   │   ├── chatRoutes.js
│   │   └── messageRoutes.js
│   ├── .env
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── Context/
│   │   ├── Pages/
│   │   ├── config/
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB Atlas account or local MongoDB
- npm or yarn

### Installation

1. **Clone the repository**
```bash
git clone <your-repo-url>
cd chat-sphere
```

2. **Setup Backend**
```bash
cd backend
npm install
```

Create a `.env` file in the backend directory:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
```

3. **Setup Frontend**
```bash
cd ../frontend
npm install
```

Create a `.env` file in the frontend directory:
```env
REACT_APP_API_URL=http://localhost:5000
REACT_APP_SOCKET_URL=http://localhost:5000
```

### Running the Application

1. **Start Backend Server**
```bash
cd backend
npm start
```
Backend runs on http://localhost:5000

2. **Start Frontend Development Server**
```bash
cd frontend
npm start
```
Frontend runs on http://localhost:3000

## 🎯 Usage

1. **Register** a new account or use the guest user option
2. **Search** for users to start a conversation
3. **Create** one-to-one or group chats
4. **Send** messages in real-time
5. **Manage** group settings (add/remove users, rename)

## 🌐 Deployment

### Backend (Render)
1. Create a new Web Service on Render
2. Connect your GitHub repository
3. Set build command: `cd backend && npm install`
4. Set start command: `cd backend && npm start`
5. Add environment variables

### Frontend (Vercel)
1. Import your GitHub repository to Vercel
2. Set root directory to `frontend`
3. Add environment variables
4. Deploy

### Database (MongoDB Atlas)
1. Create a cluster on MongoDB Atlas
2. Create a database user
3. Whitelist IP addresses
4. Copy connection string to backend `.env`

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

Built with ❤️ using the MERN stack

---

**Happy Chatting! 💬**
