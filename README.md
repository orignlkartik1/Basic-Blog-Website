# Basic Blog Website

A lightweight, full-featured blogging platform built with Flask and SQLAlchemy. Create posts, manage user accounts, and engage with comments in a simple, intuitive interface.

## 🌟 Features

- **User Authentication**: Secure user registration and login system with password hashing
- **Create & View Posts**: Write and publish blog posts with timestamps
- **Comments**: Engage with the community by commenting on posts
- **User Management**: Manage user profiles and posted content
- **Responsive Design**: Clean HTML and CSS interface
- **SQLite Database**: Lightweight, file-based database for easy deployment

## 🛠️ Tech Stack

- **Backend**: Python 3 with Flask
- **Database**: SQLite with SQLAlchemy ORM
- **Frontend**: HTML5 & CSS3
- **Authentication**: Flask-Login with password hashing (Werkzeug)
- **Forms**: Flask-WTF for secure form validation

## 📋 Prerequisites

- Python 3.7+
- pip (Python package manager)

## 🚀 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/orignlkartik1/Basic-Blog-Website.git
   cd Basic-Blog-Website
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install flask flask-sqlalchemy flask-login flask-wtf
   ```

4. **Configure the application**
   - Update `config.py` with your secret key and database settings if needed:
     ```python
     SECRET_KEY = 'your_secret_key'  # Change this to a secure key
     SQLALCHEMY_DATABASE_URI = 'sqlite:///blog.db'
     ```

5. **Run the application**
   ```bash
   python run_app.py
   ```
   The application will start at `http://localhost:5000`

## 📁 Project Structure

```
Basic-Blog-Website/
├── main.py              # Main application file with routes
├── models.py            # Database models (User, Post, Comment)
├── forms.py             # WTForms for user input validation
├── config.py            # Application configuration
├── run_app.py           # Application entry point
├── templates/           # HTML templates
├── static/              # CSS and static files
└── instance/            # Instance folder for database
```

## 🔧 Core Components

### Models
- **User**: Username and password storage with authentication methods
- **Post**: Blog posts with title, content, author, and timestamps
- **Comment**: User comments on posts with timestamps

### Routes
- `/` - Home page displaying all posts
- `/register` - User registration
- `/login` - User login
- `/logout` - User logout (login required)
- `/post/new` - Create a new post (login required)
- `/post/<post_id>` - View a post with comments and comment form

### Forms
- **RegisterForm**: Username and password fields
- **LoginForm**: Username and password validation
- **PostForm**: Title and content for new posts
- **CommentForm**: Comment submission

## 💡 Usage

1. **Register**: Click register and create a new account
2. **Login**: Log in with your credentials
3. **Create Posts**: Navigate to "New Post" and share your thoughts
4. **Browse Posts**: View all posts on the home page
5. **Comment**: Click on a post to view it and add comments
6. **Logout**: Click logout when done

## 🔐 Security Features

- Password hashing using Werkzeug
- CSRF protection via Flask-WTF
- SQL injection prevention through SQLAlchemy ORM
- Login required decorators for protected routes
- Secure session management with Flask-Login

## 📝 Environment Variables

Consider using environment variables for sensitive information:

```python
SECRET_KEY = os.environ.get('SECRET_KEY', 'your_secret_key')
SQLALCHEMY_DATABASE_URI = os.environ.get('DATABASE_URL', 'sqlite:///blog.db')
```

## 🐛 Error Handling

- **404 Error**: Custom error page for non-existent posts
- **500 Error**: Server error handling with database rollback

## 📚 Dependencies

- `flask` - Web framework
- `flask-sqlalchemy` - ORM for database operations
- `flask-login` - User session management
- `flask-wtf` - Form validation and CSRF protection
- `werkzeug` - Password hashing utilities

## 🚀 Future Enhancements

- Edit and delete posts functionality
- User profiles
- Post search and filtering
- User follow system
- Email notifications
- Comment moderation

## 📄 License

This project is open source and available for educational purposes.

## 👤 Author

[orignlkartik1](https://github.com/orignlkartik1)

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests.

---

**Happy Blogging! 📝**
