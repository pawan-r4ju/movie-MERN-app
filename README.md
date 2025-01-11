
# The Movie Hub 🎬

A full-stack movie application built using the MERN stack (MongoDB, Express.js, React.js, Node.js) with modern features and a sleek user interface.

## 📋 Features

### 👤 User Features
- 🔑 User authentication (Register/Login/Logout)
- 🎥 Browse movies with advanced filtering options
- 🔍 Search movies by name
- 🎭 Filter movies by genre and year
- 🔄 Sort movies (New/Top/Random)
- 📝 View movie details including cast and description
- ⭐ Add movie reviews and ratings
- 👤 Profile management

### 🧑‍💼 Admin Features
- 📊 Admin dashboard with real-time statistics
- 🎬 Create and manage movie genres
- ➕ Add new movies with details and images
- ✏️ Update existing movies
- ❌ Delete movies
- 💬 Manage user comments
- 📈 View user statistics


## 🛠️ Tech Stack

### 💻 Frontend
- ⚛️ React.js
- 📦 Redux Toolkit for state management
- 🔌 RTK Query for API calls
- 🧭 React Router for navigation
- 🎨 Tailwind CSS for styling
- 📱 React Icons
- 🎠 React Slick for carousels
- 🔔 React Toastify for notifications

### 🔙 Backend
- 🖥️ Node.js
- 🧑‍💻 Express.js
- 🗃️ MongoDB with Mongoose
- 🔐 JWT for authentication
- 🔒 Bcrypt for password hashing
- 📤 Multer for file uploads

##  🚀Installation

1. Clone the repository:
```bash
git clone https://github.com/pawan-r4ju/movie-MERN-app.git
```
2. **Install dependencies for both frontend and backend:**
```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
```
3. **Create a .env file in the root directory with the following variables:**
```bash
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=development
```
3. **Run the application:**
```bash
# Run both frontend and backend
npm run fullstack

# Run backend only
npm run backend

# Run frontend only
npm run frontend
```


## 📚 API Endpoints

### 👤 User Routes
- **POST** `/api/v1/users` - Register a new user  
- **POST** `/api/v1/users/auth` - Login a user  
- **POST** `/api/v1/users/logout` - Logout a user  
- **PUT** `/api/v1/users/profile` - Update user profile  

### 🎬 Movie Routes
- **GET** `/api/v1/movies/all-movies` - Retrieve all movies  
- **GET** `/api/v1/movies/specific-movie/:id` - Get details of a movie by ID  
- **GET** `/api/v1/movies/new-movies` - Fetch newly added movies  
- **GET** `/api/v1/movies/top-movies` - Fetch top-rated movies  
- **GET** `/api/v1/movies/random-movies` - Fetch random movies  
- **POST** `/api/v1/movies/create-movie` - Create a new movie (Admin only)  
- **PUT** `/api/v1/movies/update-movie/:id` - Update movie details (Admin only)  
- **DELETE** `/api/v1/movies/delete-movie/:id` - Delete a movie (Admin only)  

### 🎭 Genre Routes
- **POST** `/api/v1/genre` - Create a new genre (Admin only)  
- **PUT** `/api/v1/genre/:id` - Update a genre (Admin only)  
- **DELETE** `/api/v1/genre/:id` - Delete a genre (Admin only)  
- **GET** `/api/v1/genre/genres` - Retrieve all genres  

# 🗂️Project Structure

```plaintext
movie-MERN-app/
├── 🎬 backend/                          # Backend folder for server-side logic
│   ├── ⚙️ config/                       # Configuration files
│   │   └── 🗃️ db.js                     # Database connection setup
│   ├── 🎮 controllers/                  # Contains route controllers
│   │   ├── 🔐 authController.js         # Handles user authentication logic
│   │   ├── 🎥 movieController.js        # Handles movie-related operations
│   │   └── 🎞️ genreController.js        # Handles genre-related operations
│   ├── ⚡ middlewares/                  # Custom middleware functions
│   │   ├── 🛡️ authMiddleware.js         # Protects routes and checks user roles
│   │   └── ⚠️ errorMiddleware.js        # Handles error responses
│   ├── 🏗️ models/                       # Database models
│   │   ├── 👤 userModel.js              # Schema for user data
│   │   ├── 🎬 movieModel.js             # Schema for movie data
│   │   └── 🎭 genreModel.js             # Schema for genre data
│   ├── 🛣️ routes/                       # API route definitions
│   │   ├── 🔑 authRoutes.js             # Routes for authentication (login, register, etc.)
│   │   ├── 🎞️ movieRoutes.js            # Routes for movie-related APIs
│   │   └── 🎬 genreRoutes.js            # Routes for genre-related APIs
│   ├── 🧰 utils/                        # Utility functions
│   │   └── 🔑 generateToken.js          # Generates JWT for authentication
│   ├── 🌿 .env                          # Environment variables
│   ├── 🖥️ server.js                     # Main server file
│   └── 📦 package.json                  # Backend dependencies and scripts
├── 💻 frontend/                         # Frontend folder for client-side logic
│   ├── 📂 src/                          # Source files
│   │   ├── 🧩 components/               # Reusable UI components
│   │   │   ├── 🎞️ MovieCard.js          # Component to display a movie card
│   │   │   ├── 🌐 Navbar.js             # Top navigation bar
│   │   │   └── 🦶 Footer.js             # Footer section
│   │   ├── 🏠 pages/                    # Main application pages
│   │   │   ├── 🏡 HomePage.js           # Home page with movies listing
│   │   │   ├── 🎬 MoviePage.js          # Detailed view of a movie
│   │   │   └── 🛠️ AdminPage.js          # Admin page for managing movies and genres
│   │   ├── ⚙️ redux/                    # Redux state management
│   │   │   ├── 📦 store.js              # Configures the Redux store
│   │   │   ├── 🧃 slices/               # Redux slices for state
│   │   │   │   ├── 🔑 authSlice.js      # Authentication state management
│   │   │   │   ├── 🎥 movieSlice.js     # Movie state management
│   │   │   │   └── 🎭 genreSlice.js     # Genre state management
│   │   ├── 🖼️ assets/                   # Static assets (images, icons, etc.)
│   │   │   └── 🖼️ images/               # Image files
│   │   ├── 📱 App.js                    # Main app component
│   │   ├── 🚀 index.js                  # Entry point for the React app
│   │   └── 📦 package.json              # Frontend dependencies and scripts
├── 📂 public/                           # Public files accessible to the browser
│   ├── 🗂️ index.html                    # Main HTML file
│   └── 🖍️ favicon.ico                   # Favicon for the browser tab



## License

- MIT 📝  

## Author

- **Pawan Raju** 👨‍💻  

## Made with ❤️ and JavaScript. 💻
ipt.




