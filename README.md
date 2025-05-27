# Wanderlust 🌍

A full-stack travel website built with Node.js, Express.js, MongoDB, and EJS. Discover and share amazing travel destinations around the world!

## 🚀 Features

- **User Authentication & Authorization**: Secure user registration, login, and session management
- **Travel Listings**: Browse and search through various travel destinations
- **CRUD Operations**: Create, read, update, and delete travel listings
- **User Profiles**: Personalized user accounts and profiles
- **Responsive Design**: Mobile-friendly interface for all devices
- **Image Upload**: Share stunning photos of destinations
- **Reviews & Ratings**: Rate and review travel destinations
- **Search & Filter**: Find destinations by location, price, or category

## 🛠️ Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose ODM
- **Template Engine**: EJS (Embedded JavaScript)
- **Authentication**: Passport.js with local strategy
- **Session Management**: Express-session
- **File Upload**: Multer for image handling
- **Styling**: Bootstrap CSS framework
- **Architecture**: MVC (Model-View-Controller) pattern

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/) (v4.4 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

## ⚡ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/wanderlust.git
   cd wanderlust
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory and add:
   ```env
   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/wanderlust
   SESSION_SECRET=your-secret-key-here
   CLOUDINARY_CLOUD_NAME=your-cloudinary-name
   CLOUDINARY_API_KEY=your-cloudinary-api-key
   CLOUDINARY_API_SECRET=your-cloudinary-api-secret
   ```

4. **Start MongoDB**
   Make sure MongoDB is running on your system:
   ```bash
   mongod
   ```

5. **Run the application**
   ```bash
   npm start
   ```
   
   For development with auto-restart:
   ```bash
   npm run dev
   ```

6. **Access the application**
   Open your browser and navigate to `http://localhost:3000`

## 📁 Project Structure

```
wanderlust/
│
├── models/              # Database models (User, Listing)
│   ├── user.js
│   └── listing.js
│
├── routes/              # Express routes
│   ├── auth.js          # Authentication routes
│   ├── listings.js      # Listing CRUD routes
│   └── users.js         # User profile routes
│
├── controllers/         # Route controllers (MVC)
│   ├── authController.js
│   ├── listingController.js
│   └── userController.js
│
├── views/               # EJS templates
│   ├── layouts/         # Layout templates
│   ├── partials/        # Reusable components
│   ├── listings/        # Listing-related views
│   ├── users/           # User-related views
│   └── auth/            # Authentication views
│
├── public/              # Static files
│   ├── css/
│   ├── js/
│   └── images/
│
├── middleware/          # Custom middleware
│   ├── auth.js          # Authentication middleware
│   └── validation.js    # Input validation
│
├── config/              # Configuration files
│   └── database.js
│
├── utils/               # Utility functions
│   └── helpers.js
│
├── app.js               # Main application file
├── package.json
└── README.md
```

## 🔐 Authentication & Authorization

The application implements secure user authentication and authorization:

- **Registration**: Users can create new accounts with email and password
- **Login/Logout**: Secure session-based authentication
- **Password Hashing**: Passwords are hashed using bcrypt
- **Route Protection**: Middleware protects authenticated routes
- **Authorization**: Users can only modify their own listings
- **Session Management**: Secure session handling with express-session

## 🎨 Key Features Implementation

### User Authentication
- Passport.js local strategy for username/password authentication
- Session-based authentication with secure cookies
- Password hashing with bcrypt

### CRUD Operations
- **Create**: Add new travel listings with images
- **Read**: View all listings and individual listing details
- **Update**: Edit existing listings (owner only)
- **Delete**: Remove listings (owner only)

### Database Models
- **User Model**: Stores user credentials and profile information
- **Listing Model**: Stores travel destination data with owner references

## 🚀 Deployment

### Local Deployment
Follow the installation steps above.

### Production Deployment (Heroku)
1. Create a Heroku app
2. Set up MongoDB Atlas for cloud database
3. Configure environment variables in Heroku
4. Deploy using Git:
   ```bash
   git add .
   git commit -m "Deploy to Heroku"
   git push heroku main
   ```

## 📖 API Routes

### Authentication Routes
- `GET /register` - Show registration form
- `POST /register` - Register new user
- `GET /login` - Show login form
- `POST /login` - Login user
- `POST /logout` - Logout user

### Listing Routes
- `GET /listings` - Show all listings
- `GET /listings/new` - Show create listing form
- `POST /listings` - Create new listing
- `GET /listings/:id` - Show specific listing
- `GET /listings/:id/edit` - Show edit form
- `PUT /listings/:id` - Update listing
- `DELETE /listings/:id` - Delete listing

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- Express.js community for the excellent web framework
- MongoDB for the flexible database solution
- EJS for the simple templating engine
- Bootstrap for responsive design components
- Passport.js for authentication middleware

---

⭐ **If you found this project helpful, please give it a star!** ⭐
