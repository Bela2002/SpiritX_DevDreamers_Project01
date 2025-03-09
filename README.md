# SpiritX_DevDreamers_Project01

##SecureConnect - User Authentication System

SecureConnect is a user authentication system built using HTML, CSS, Bootstrap, and PHP. It allows users to register, log in, and manage their accounts securely. The system uses a MySQL database to store user information.

##Table of Contents

1.Guidelines for Stage 1

2.Instructions to Run the Project

3.Database Setup and Configuration

4.Assumptions

5.Additional Features

6.Screenshots

##Guidelines for Stage 1

User Registration: Users can register by providing their email, username, and password. The password is hashed before storing in the database.

User Login: Registered users can log in using their username and password.

Password Validation: Passwords must meet complexity requirements (at least one lowercase letter, one uppercase letter, and one special character).

Error Handling: Clear error messages are displayed for invalid inputs, duplicate emails, or usernames.

Session Management: Users remain logged in across pages using PHP sessions.

##Instructions to Run the Project

#Prerequisites

Web Server: Apache.

PHP: PHP 7.4 or higher.

MySQL: MySQL or MariaDB.

#Steps to Run

1.Clone the Repository:
https://github.com/Bela2002/SpiritX_DevDreamers_Project01.git

cd secureconnect

2.Set Up the Database:

Import the provided SQL dump (secureconnect.sql) into your MySQL database.

Update the database configuration in config.php with your database credentials.

3.Configure the Web Server:

Place the project folder in your web server's root directory (e.g., htdocs for XAMPP or www for WAMP).

Ensure the server is running.

4.Access the Application:

Open your browser and navigate to http://localhost/SpiritX_DevDreamers_Project01

##Database Setup and Configuration

#Database Schema

The users table is created with the following structure:

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(255) NOT NULL UNIQUE,
    username VARCHAR(255) NOT NULL UNIQUE,
    mypassword VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

1.Steps to Set Up the Database

Create the Database:

CREATE DATABASE secureconnect;
USE secureconnect;

2.Import the SQL Dump:

Use the provided SQL dump file (secureconnect.sql) to create the users table and populate it with sample data (if any).

3.Update config.php:

Open config.php and update the database connection details:

$host = 'localhost';
$dbname = 'secureconnect';
$user = 'root';
$pass = '';

##Assumptions

1.Email and Username Uniqueness: Both email and username must be unique in the database.

2.Password Complexity: Passwords must contain at least one lowercase letter, one uppercase letter, and one special character.

3.Session Management: Users are logged out after closing the browser or after a session timeout.

4.Error Messages: Clear error messages are displayed for invalid inputs or database errors.

##Additional Features

1.Password Strength Indicator: A dynamic password strength indicator guides users to create strong passwords.

2.Automatic Redirection: After successful registration, users are automatically redirected to the login page after 2 seconds.

3.Responsive Design: The application is fully responsive and works on all devices (desktop, tablet, mobile).

4.Secure Password Storage: Passwords are hashed using PHP's password_hash() function.

##Screenshots

Users Table in phpMyAdmin
![image](https://github.com/user-attachments/assets/c1fbe01d-4083-455e-aff6-b369242674bc)

Registration Page
![image](https://github.com/user-attachments/assets/30c7224e-ee80-480a-875e-6baf591c89f6)

Login Page
![image](https://github.com/user-attachments/assets/f77a0062-91f7-4834-a245-549402580925)


