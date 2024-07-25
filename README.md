# Django Login Registration with JWT Tokens

A simple Django application for user registration, login, and JWT-based authentication using Django REST framework and Swagger for API documentation.

## Features

- User registration
- User login with JWT authentication
- Secure JWT token handling
- API documentation with Swagger

## Requirements

- Python 3.8+
- Django 3.0+
- Django REST framework
- drf-yasg

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/aneeshvishwanaath/Django-Login-Registration-JWT-Tokens.git
   cd Django-Login-Registration-JWT-Tokens
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Apply the migrations:

   ```bash
   python manage.py migrate
   ```

5. Create a superuser:

   ```bash
   python manage.py createsuperuser
   ```

6. Collect static files:

   ```bash
   python manage.py collectstatic
   ```

7. Run the development server:

   ```bash
   python manage.py runserver
   ```

## API Endpoints

### User Registration

- URL: `/api/register/`
- Method: `POST`
- Payload:
  ```json
  {
    "username": "your_username",
    "password": "your_password"
  }
  ```
- Response:
  ```json
  {
    "id": 1,
    "username": "your_username"
  }
  ```

### User Login

- URL: `/api/login/`
- Method: `POST`
- Payload:
  ```json
  {
    "username": "your_username",
    "password": "your_password"
  }
  ```
- Response:
  ```json
  {
    "refresh": "refresh_token",
    "access": "access_token"
  }
  ```

### User Profile

- URL: `/api/user/`
- Method: `GET`, `PATCH`, `DELETE`
- Authentication: `Bearer <access_token>`
- Response:
  ```json
  {
    "id": 1,
    "username": "your_username"
  }
  ```

### Welcome Message

- URL: `/api/welcome/`
- Method: `GET`
- Authentication: `Bearer <access_token>`
- Response:
  ```json
  {
    "message": "Welcome, your_username!"
  }
  ```

## API Documentation

Swagger documentation is available at `/swagger/`.

## License

This project is licensed under the MIT License.
```
