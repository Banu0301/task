# News App - Full Stack Application

A modern news application built with React, Node.js, Express, MongoDB, and NewsAPI integration. Features user authentication, personalized news feeds, bookmarking, and responsive design.

## Features

- **User Authentication**: Secure JWT-based authentication with registration and login
- **Personalized News Feed**: Customizable news based on user preferences
- **News Categories**: Browse news by categories (Business, Technology, Sports, etc.)
- **Country-based News**: Filter news by different countries
- **Search Functionality**: Search for specific news articles
- **Bookmarking**: Save articles for later reading
- **User Preferences**: Customize categories, countries, and language preferences
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Tech Stack

### Frontend
- React 19
- Material-UI (MUI)
- React Router DOM
- Axios
- Context API for state management

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- bcryptjs for password hashing
- NewsAPI integration

## Prerequisites

Before running this application, make sure you have:

- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)
- NewsAPI key (get it from [NewsAPI.org](https://newsapi.org/))

## Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd news-app
```

### 2. Backend Setup
```bash
cd client/server
npm install
```

Create a `.env` file in the `client/server` directory:
```env
# MongoDB Configuration
MONGODB_URI=mongodb://localhost:27017/newsapp
# Or use MongoDB Atlas: mongodb+srv://username:password@cluster.mongodb.net/newsapp

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_here_change_in_production
JWT_EXPIRE=7d

# NewsAPI Configuration
NEWS_API_KEY=your_newsapi_key_here

# Server Configuration
PORT=5000
NODE_ENV=development
```

### 3. Frontend Setup
```bash
cd client
npm install
```

Create a `.env` file in the `client` directory:
```env
REACT_APP_API_URL=http://localhost:5000/api
```

## Running the Application

### Development Mode

1. **Start the Backend Server**:
```bash
cd client/server
npm run dev
```
The server will run on http://localhost:5000

2. **Start the Frontend**:
```bash
cd client
npm start
```
The React app will run on http://localhost:3000

### Production Mode

1. **Build the Frontend**:
```bash
cd client
npm run build
```

2. **Start the Backend**:
```bash
cd client/server
npm start
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `POST /api/auth/refresh` - Refresh JWT token

### News
- `GET /api/news/headlines` - Get top headlines
- `GET /api/news/search` - Search news articles
- `GET /api/news/personalized` - Get personalized news (requires auth)
- `GET /api/news/category/:category` - Get news by category
- `GET /api/news/country/:country` - Get news by country
- `GET /api/news/sources` - Get news sources

### User Management
- `GET /api/user/profile` - Get user profile
- `PUT /api/user/profile` - Update user profile
- `PUT /api/user/preferences` - Update user preferences
- `GET /api/user/bookmarks` - Get user bookmarks
- `POST /api/user/bookmarks` - Add bookmark
- `DELETE /api/user/bookmarks/:id` - Remove bookmark

## Deployment

### Frontend Deployment (Vercel)

1. **Install Vercel CLI**:
```bash
npm i -g vercel
```

2. **Deploy**:
```bash
cd client
vercel
```

3. **Set Environment Variables** in Vercel dashboard:
- `REACT_APP_API_URL`: Your backend API URL

### Backend Deployment (Render)

1. **Create a new Web Service** on Render
2. **Connect your repository**
3. **Set the following**:
   - Build Command: `cd client/server && npm install`
   - Start Command: `cd client/server && npm start`
   - Root Directory: `/`

4. **Set Environment Variables**:
   - `MONGODB_URI`: Your MongoDB connection string
   - `JWT_SECRET`: Your JWT secret key
   - `NEWS_API_KEY`: Your NewsAPI key
   - `NODE_ENV`: `production`

### Database Setup (MongoDB Atlas)

1. **Create a MongoDB Atlas account**
2. **Create a new cluster**
3. **Create a database user**
4. **Whitelist your IP address**
5. **Get the connection string** and update `MONGODB_URI`

## Environment Variables

### Backend (.env in client/server/)
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d
NEWS_API_KEY=your_newsapi_key
PORT=5000
NODE_ENV=production
```

### Frontend (.env in client/)
```env
REACT_APP_API_URL=your_backend_api_url
```

## Features Overview

### User Authentication
- Secure registration and login system
- JWT-based authentication
- Password hashing with bcryptjs
- Protected routes

### News Integration
- Real-time news from NewsAPI
- Multiple categories and countries
- Search functionality
- Caching for better performance

### User Experience
- Responsive Material-UI design
- Personalized news feed
- Bookmark management
- User preference customization

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support, please open an issue in the repository or contact the development team.
#   t a s k w o r k  
 #   t a s k w o r k  
 #   t a s k  
 #   n e w t a s k  
 