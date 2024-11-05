# Authentication-Lv3

# User Authentication System with Express, Passport, PostgreSQL, and Google OAuth

This project implements a user authentication system with support for local and Google OAuth login, using Express, Passport, and PostgreSQL.

## Table of Contents

- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Dependencies](#dependencies)
- [Features](#features)
- [License](#license)

## Installation

1. **Clone the repository:**

   ```bash
   git clone (https://github.com/jbolan12/Authentication-Lv3)

   Navigate to the project directory:

bash
cd your-repo-name


## Install dependencies:

bash
npm install

## Set up PostgreSQL:

Ensure that PostgreSQL is installed and running on your system.
Create a database and a users table with email and password fields.

## Set up Google OAuth Credentials:

Go to the Google Developer Console.
Create a new project and enable the Google+ API or OAuth consent screen.
Generate OAuth 2.0 credentials and copy the Client ID and Client Secret.


## Environment Variables:

-> Create a .env file in the root of your project and add the following keys:

plaintext

SESSION_SECRET=your-session-secret
PG_USER=your-postgres-username
PG_HOST=localhost
PG_DATABASE=your-database-name
PG_PASSWORD=your-database-password
PG_PORT=5432
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret


## Usage
Start the server:

bash
npm start


## Access the application:

The application runs on http://localhost:3000.
Visit http://localhost:3000 to access the home page.


## Authentication Routes:

/register: Register a new account.
/login: Log in with local authentication.
/auth/google: Log in with Google OAuth.
/secrets: A protected route accessible only to authenticated users.
/logout: Log out of the application.


## File Structure
plaintext

├── public
│   └── styles.css          # Static CSS files
├── views
│   ├── home.ejs            # Home page
│   ├── login.ejs           # Login page
│   ├── register.ejs        # Registration page
│   └── secrets.ejs         # Protected secrets page
├── .env                    # Environment variables
└── app.js                  # Main application file


## Dependencies
Express: Web framework for Node.js.
Passport: Authentication middleware for Node.js.
passport-local: Local authentication strategy for Passport.
passport-google-oauth2: Google OAuth strategy for Passport.
bcrypt: For hashing passwords.
pg: PostgreSQL client for Node.js.
dotenv: For managing environment variables.
express-session: Middleware for managing sessions.


## Features
Local Authentication: Users can register and log in using their email and password.
Google OAuth: Users can log in using their Google accounts.
Session Management: Secure session management using cookies.
Protected Routes: Access control for sensitive pages based on user authentication status.


## License
This project is licensed under the MIT License.
