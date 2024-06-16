Goodreads API
This repository contains an Express.js application that serves as a backend API for a simplified version of Goodreads, allowing users to manage books and user accounts.

Features
User Authentication: Register and login functionalities using bcrypt for password hashing and JWT (JSON Web Tokens) for authentication.
Book Management: CRUD operations (Create, Read, Update, Delete) for books.
User Profile: Fetch user details based on authentication.
Author Books: Fetch books written by a specific author.
Prerequisites
Node.js installed on your local machine.
SQLite database (file goodreads.db) setup.
Installation
Clone the repository:

bash
Copy code
git clone <repository-url>
cd <repository-name>
Install dependencies:

bash
Copy code
npm install
Start the server:

bash
Copy code
npm start
The server will start at http://localhost:3000.

API Endpoints
User Routes
Register User: POST /users/

Register a new user with username, name, password, gender, and location.

User Login: POST /login/

Authenticate user and generate JWT token for subsequent requests.

User Profile: GET /profile/

Fetch logged-in user details.

Book Routes
Get All Books: GET /books/

Fetch all books from the database.

Get Single Book: GET /books/:bookId/

Fetch details of a specific book by bookId.

Add Book: POST /books/

Add a new book to the database.

Update Book: PUT /books/:bookId/

Update details of a book by bookId.

Delete Book: DELETE /books/:bookId/

Delete a book from the database by bookId.

Get Author's Books: GET /authors/:authorId/books/

Fetch books written by a specific author identified by authorId.

Middleware
Authentication: authenticateToken

Middleware to verify JWT token for protected routes.

Database Schema
The application uses SQLite with the following schema:

user: Stores user details including username, name, password hash, gender, and location.
book: Stores book details such as title, author_id, rating, description, etc.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Inspired by Goodreads.
Built with Express.js, SQLite, bcrypt, and JWT.
