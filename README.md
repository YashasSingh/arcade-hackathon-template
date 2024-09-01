
# Flask Web Application

## Overview

This project is a Flask-based web application template that includes user authentication, authorization, an admin dashboard, and enhanced security features such as account locking after multiple failed login attempts and two-factor authentication (2FA). 

## Features

- **User Registration and Login**: Users can sign up and log in to access the application.
- **User Authentication**: Passwords are securely hashed using `werkzeug.security`.
- **User Authorization**: Different user roles (`user`, `admin`) are supported. Admins have access to an admin dashboard to manage users.
- **Admin Dashboard**: Admins can view and delete users.
- **Logging**: Detailed logging of user actions, login attempts, and admin activities.
- **Account Locking**: Accounts are locked after three failed login attempts.
- **Two-Factor Authentication (2FA)**: An additional layer of security using email-based 2FA.

## Getting Started

### Prerequisites

- Python 3.x
- Flask
- Flask-SQLAlchemy
- Flask-Mail
- Flask-WTF

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/flask-web-app.git
   cd flask-web-app
   ```

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up the Database**

   Initialize the SQLite database and create the necessary tables:

   ```bash
   flask db init
   flask db migrate
   flask db upgrade
   ```

4. **Configure Environment Variables**

   Create a `.env` file in the root directory and set the following environment variables:

   ```env
   SECRET_KEY='your_secret_key'
   SQLALCHEMY_DATABASE_URI='sqlite:///site.db'
   MAIL_SERVER='smtp.googlemail.com'
   MAIL_PORT=587
   MAIL_USE_TLS=1
   MAIL_USERNAME='your_email@example.com'
   MAIL_PASSWORD='your_email_password'
   ```

5. **Run the Application**

   Start the Flask development server:

   ```bash
   flask run
   ```

6. **Access the Application**

   Open your web browser and go to `http://127.0.0.1:5000/`.

## Usage

- **Sign Up**: Create a new user account.
- **Log In**: Access your account with your username and password.
- **Admin Dashboard**: Admin users can manage other users from the dashboard.
- **Two-Factor Authentication**: After logging in, a 2FA code will be sent to your email. Enter this code to complete the login process.

## Security Features

- **Password Hashing**: All passwords are hashed using `werkzeug.security`.
- **Account Locking**: Accounts are locked after three failed login attempts to prevent brute-force attacks.
- **Two-Factor Authentication (2FA)**: Enhances security by requiring a second factor (email-based code) to complete the login.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.

## Contributing

Feel free to submit issues and pull requests. For major changes, please open an issue first to discuss what you would like to change.

