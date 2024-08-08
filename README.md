# Advanced Authentication with Flask

This repository contains a Flask-based web application that demonstrates a simple authentication system with user registration, login, and session management. The project uses SQLite as the database and integrates Flask-Login for managing user sessions.

## Features

- **User Registration**: New users can create an account with a unique email address.
- **User Login**: Registered users can log in with their email and password.
- **Password Hashing**: User passwords are securely hashed using the `pbkdf2:sha256` algorithm.
- **Protected Routes**: Certain routes are protected and accessible only to logged-in users.
- **Session Management**: Users remain logged in until they log out.
- **File Download**: Logged-in users can download a file from the server.

## Project Structure

```plaintext
.
├── main.py                 # Main Flask application file
├── templates/              # Directory containing HTML templates
│   ├── base.html           # Base template with common layout
│   ├── index.html          # Homepage template
│   ├── login.html          # Login page template
│   └── secrets.html        # Secrets page template (protected)
├── static/                 # Directory containing static files (e.g., CSS, images)
│   ├── css/
│   │   └── styles.css      # Custom CSS styles
│   └── files/
│       └── cheat_sheet.pdf # File available for download to logged-in users
└── README.md               # Project README file
```

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Prathamesh326/Advanced-authentication-with-flask.git
   cd Advanced-authentication-with-flask
   ```

2. **Create and activate a virtual environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database**:
   ```bash
   python main.py
   ```

5. **Run the Flask application**:
   ```bash
   flask run
   ```

   The application will be available at `http://127.0.0.1:5000`.

## Usage

- **Home Page**: The homepage provides links to login or register if the user is not authenticated.
- **Registration**: New users can sign up by providing their name, email, and password.
- **Login**: Registered users can log in with their credentials. If the email or password is incorrect, an appropriate message is displayed.
- **Secrets Page**: A protected page that only logged-in users can access. This page displays the user's name and allows them to download a file.
- **Logout**: Users can log out by clicking the "Log Out" link in the navigation bar.

## Dependencies

- **Flask**: A micro web framework for Python.
- **Flask-Login**: Provides user session management for Flask.
- **Flask-SQLAlchemy**: Adds SQLAlchemy support to Flask applications.
- **Werkzeug**: Provides password hashing utilities.

---

**Note**: This project is a demonstration of a basic authentication system using Flask and should not be used as-is for production environments. Always ensure to follow best practices for security, especially when handling user data.
```

This README provides an overview of the project, installation instructions, usage details, and additional information on contributions and licensing. You can place this content in a `README.md` file in your GitHub repository.
