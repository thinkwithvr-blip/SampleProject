# Python Login System with Database

A complete login system built with Flask and SQLite database, featuring user authentication, registration, and session management.

## Features

- User registration and login
- Password hashing for security
- Session management
- SQLite database integration
- Modern, responsive UI with Bootstrap
- Flash messages for user feedback
- Protected dashboard area

## Installation

1. Install the required dependencies:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
python app.py
```

3. Open your browser and navigate to `http://localhost:5000`

## Default Credentials

A default admin user is created automatically:
- Username: `admin`
- Password: `admin123`

## Usage

1. **Login**: Use the default credentials or register a new account
2. **Register**: Create a new user account with username, email, and password
3. **Dashboard**: Access the protected area after successful login
4. **Logout**: End your session and return to the login page

## Database

The application uses SQLite database (`users.db`) which is created automatically. The database contains a `User` table with the following fields:
- `id`: Primary key
- `username`: Unique username
- `email`: Unique email address
- `password_hash`: Hashed password

## Security Features

- Passwords are hashed using Werkzeug's security functions
- Session-based authentication
- Input validation
- CSRF protection through Flask's secret key

## File Structure

```
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── templates/            # HTML templates
│   ├── base.html         # Base template
│   ├── login.html        # Login page
│   ├── register.html     # Registration page
│   └── dashboard.html    # Protected dashboard
└── users.db              # SQLite database (created automatically)
```

## Customization

- Change the secret key in `app.py` for production use
- Modify the database URI to use PostgreSQL, MySQL, or other databases
- Customize the UI by editing the HTML templates and CSS
- Add additional user fields by modifying the User model