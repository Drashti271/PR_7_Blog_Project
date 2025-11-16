# PR_7_BLOG_PROJECT Documentation

## 1. Overview

PR_7_BLOG_PROJECT is a blog application built with Node.js, Express.js, MongoDB, and EJS. It includes features such as user management, blog posting, file uploads, and routing with MVC architecture.

---

## 2. Project Structure

```
PR_7_BLOG_PROJECT/
│
├── configs/        # Database & other configuration files
├── controllers/    # Request handlers (business logic)
├── middlewares/    # Auth, file upload, validations, etc.
├── models/         # Mongoose models (User, Blog, etc.)
├── node_modules/   # Dependencies
├── public/         # Static files (CSS, JS, images)
├── routers/        # Express route files
├── uploads/        # Uploaded files
├── views/          # EJS templates
│
├── .env            # Environment variables
├── index.js        # Main server entry file
├── package.json    # Project metadata & dependencies
├── package-lock.json
└── README.md
```

---

## 3. Installation

### Step 1: Install Dependencies

Run the command:

```
npm install
```

### Step 2: Create `.env` File

Add required environment variables:

```
PORT=5000
MONGO_URL=mongodb://localhost:27017/blogDB
SECRET_KEY=your_secret_key
```

### Step 3: Start the Server

```
nodemon index.js
```

OR

```
node index.js
```

---

## 4. Configs

### `configs/db.js`

Connects the application to MongoDB using Mongoose.

---

## 5. Models

### Common Models:

* **User Model** – Stores user information
* **Blog Model** – Stores blog posts

Each model defines schema, datatypes, and validation rules.

---

## 6. Controllers

Controllers contain the actual logic for handling requests.
Examples:

* `authController.js` – Signup, login, logout
* `blogController.js` – Create, update, delete blog
* `adminController.js` – Dashboard and admin management

Each function returns views or JSON responses.

---

## 7. Middlewares

Used for:

* Authentication (checking login)
* File Upload using Multer
* Error handling

---

## 8. Routers

Routes link URLs to controller functions.
Examples:

```
router.get('/', homePage)
router.post('/signup', signup)
router.post('/blog/add', upload.single('image'), addBlog)
```

---

## 9. Views (EJS Templates)

Contains all frontend pages such as:

* Home Page
* Blog Page
* Login / Signup Page
* Admin Dashboard

Uses EJS templating and Bootstrap/CSS for styling.

---

## 10. Public Folder

For static frontend files:

* CSS
* JavaScript
* Images

Served using Express static middleware.

---

## 11. Uploads

Stores uploaded blog images or profile pictures.

---

## 12. index.js (Main Entry File)

Configures:

* Express server
* Middleware
* Route imports
* MongoDB connection

Starts the server on defined port.

---

## 13. How to Run the Project

1. Install dependencies
2. Start MongoDB service
3. Run application
4. Visit in browser:

```
http://localhost:5000
```

---

## 14. Future Enhancements

* Add JWT-based authentication
* Comment system
* Categories & tags
* Admin panel improvements

---

## 15. Conclusion

This project demonstrates a complete MVC-based blog system using Node.js, Express, and MongoDB. You can expand it into a full-featured content management system.
