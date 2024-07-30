# H2Rwanda Login

This README provides an overview of the H2Rwanda Login Flask application, including setup instructions and a brief explanation of the project's components.

## Introduction

H2Rwanda is a Flask-based web application designed to manage and deliver water-related products and services. The app provides functionalities for user registration, login, data management, and product listing.

## Features

- User authentication and authorization
- Admin and user dashboards
- Product listing with JSON response
- User data management
- Admin user management

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/cysron-b/login.git
    cd login
    ```

2. **Create and activate a virtual environment:**

    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

3. **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Initialize the SQLite database:**

    ```bash
    flask db init
    flask db migrate
    flask db upgrade
    ```

## Configuration

Update the Flask configuration settings in `app.py`:

```python
app.config['SECRET_KEY'] = 'your_secret_key'
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///' + os.path.join(app.instance_path, 'db.sqlite')
```

## Usage

1. **Run the application:**

    ```bash
    flask run
    ```

2. **Access the application:**

    Open a web browser and go to `http://127.0.0.1:5000`

## Routes

- `/` - Redirects to the registration page
- `/login` - User login
- `/register` - User registration
- `/user_page` - User dashboard (login required)
- `/admin_page` - Admin dashboard (login required, admin only)
- `/add_user` - Admin user addition (login required, admin only)
- `/logout` - User logout
- `/products` - Returns a JSON list of products
- 
## Slides
Canva: https://www.canva.com/design/DAGMUcS37_k/RV7Eeoqj-i4AqSJkD2QQag/edit?utm_content=DAGMUcS37_k&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
