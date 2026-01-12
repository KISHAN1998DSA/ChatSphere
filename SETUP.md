# Chat-Sphere Setup Guide

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm or yarn
- MongoDB Atlas account (or local MongoDB)

## Backend Setup

1. **Navigate to backend directory**
```bash
cd backend
```

2. **Install dependencies**
```bash
npm install
```

3. **Create environment file**

Create a `.env` file in the `backend` directory with the following variables:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key
NODE_ENV=development
```

**Getting MongoDB URI:**
- Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- Create a free cluster
- Click "Connect" → "Connect your application"
- Copy the connection string and replace `<password>` with your database password

**JWT Secret:**
- Generate a random secret key (can use any random string)
- Example: `mysupersecretkey123!@#`

4. **Start the backend server**
```bash
npm start
```

The backend server will run on http://localhost:5000

## Frontend Setup

1. **Navigate to frontend directory**
```bash
cd frontend
```

2. **Install dependencies**
```bash
npm install
```

3. **Start the development server**
```bash
npm start
```

The frontend will run on http://localhost:3000

## Testing the Application

### Create Test Users

1. Open http://localhost:3000 in your browser
2. Click on "Sign Up" tab
3. Create a new user account
4. Open another browser (or incognito window)
5. Create another user account

### Test One-to-One Chat

1. Login with User 1
2. Click "Search User" in the top left
3. Search for User 2 by name or email
4. Click on User 2 to start a chat
5. Send a message
6. In the other browser, login with User 2
7. You should see the message in real-time!

### Test Group Chat

1. Click "New Group Chat" button
2. Enter a group name
3. Search and add multiple users
4. Click "Create Chat"
5. Send messages in the group
6. Other users will receive messages in real-time

### Test Features

- ✅ Real-time messaging
- ✅ Typing indicators
- ✅ Notifications
- ✅ User search
- ✅ Group chat creation
- ✅ Add/remove users from groups
- ✅ Rename groups
- ✅ Profile viewing

## Guest User Credentials

For quick testing, click "Get Guest User Credentials" on the login page:
- Email: guest@example.com
- Password: 123456

**Note:** You'll need to create this user first via the signup page.

## Troubleshooting

### Backend won't start
- Check if MongoDB URI is correct
- Ensure MongoDB Atlas allows connections from your IP
- Verify all environment variables are set

### Frontend won't connect to backend
- Ensure backend is running on port 5000
- Check proxy configuration in `frontend/package.json`
- Clear browser cache and restart

### Real-time messages not working
- Check browser console for Socket.IO errors
- Ensure both frontend and backend are running
- Verify CORS settings in backend

## Production Deployment

### Backend (Render)
1. Push code to GitHub
2. Create new Web Service on Render
3. Connect GitHub repository
4. Set build command: `cd backend && npm install`
5. Set start command: `cd backend && npm start`
6. Add environment variables in Render dashboard

### Frontend (Vercel)
1. Push code to GitHub
2. Import project to Vercel
3. Set root directory to `frontend`
4. Add environment variables:
   - `REACT_APP_API_URL=your_render_backend_url`
   - `REACT_APP_SOCKET_URL=your_render_backend_url`
5. Deploy

## Features Overview

### Authentication
- JWT-based secure authentication
- Password hashing with bcrypt
- Persistent login with localStorage

### Real-Time Messaging
- Socket.IO for instant message delivery
- Typing indicators
- Online/offline status
- Message notifications

### Chat Features
- One-to-one messaging
- Group chats (3+ users)
- Search users
- View user profiles
- Chat history

### Group Management
- Create groups
- Add/remove members
- Rename groups
- Admin controls
- Leave group

## Tech Stack

**Frontend:**
- React 18
- Chakra UI
- Socket.IO Client
- Axios
- React Router

**Backend:**
- Node.js
- Express.js
- MongoDB + Mongoose
- Socket.IO
- JWT + bcrypt

---

**Happy Chatting! 💬**
