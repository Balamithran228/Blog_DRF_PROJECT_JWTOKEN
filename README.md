# Django Rest Framework Blog API

This Django Rest Framework (DRF) Blog API project provides a comprehensive solution for building a blog platform with user authentication, user profile management, post categories, comments, and liking functionality. The project utilizes Django, Django Rest Framework, and the DRF Spectacular package for API documentation.

## Features

### User Authentication

- **JWT-based Authentication:** Secure authentication mechanism using JSON Web Tokens (JWT) for user login and registration.

### User Management

- **User Registration and Login Endpoints:** Implementation of user registration, login, and logout endpoints with JWT tokens.
  
- **User Profile Management:** Endpoints to get and update user information, user profile, and user avatar.

### Blog Functionality

- **Post Categories:** CRUD operations for managing post categories.

- **Blog Posts:** CRUD operations for creating, reading, updating, and deleting blog posts.

- **Comments:** Ability to add, view, edit, and delete comments on blog posts.

- **Like/Dislike Posts:** Functionality to like or dislike a post with dedicated API endpoints.

### API Documentation

- **DRF Spectacular Integration:** Automatic generation of interactive API documentation using DRF Spectacular. Explore endpoints, request/response schemas, and authentication details easily.

## Project Structure

- **users:** Django app handling user-related functionality, including authentication and profile management.

- **posts:** Django app responsible for blog-related functionality, including posts, categories, comments, and liking.

- **config:** Project-level configuration, including settings and URL routing.

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```

2. Create a virtual environment and install dependencies:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use 'venv\Scripts\activate'
   pip install -r requirements.txt
   ```

3. Apply database migrations:

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. Create a superuser for admin access:

   ```bash
   python manage.py createsuperuser
   ```

5. Run the development server:

   ```bash
   python manage.py runserver
   ```

## API Endpoints

### Users

- **Register:** `/users/register/` - Create a new user.
- **Login:** `/users/login/` - Authenticate existing users using email and password.
- **Logout:** `/users/logout/` - Logout users.
- **User Info:** `/users/` - Get and update user information.
- **User Profile:** `/users/profile/` - Get and update user profile.
- **User Avatar:** `/users/profile/avatar/` - Get and update user avatar.

### Blog

- **Post Categories:** `/post/categories/` - List and retrieve post categories.
- **Posts:** `/post/` - CRUD operations for blog posts.
- **Comments:** `/post/{post_id}/comment/` - CRUD operations for comments on a specific post.
- **Like/Dislike Post:** `/post/like/{post_id}/` - Like or dislike a post.

### API Documentation

- **DRF Spectacular:** Explore the API documentation using the automatic generation provided by DRF Spectacular. Visit the [Swagger UI](/swagger-ui/) endpoint when the server is running.

## Testing the API

You can use tools like [Postman](https://www.postman.com/) or explore the built-in browsable API to test the functionality of various endpoints.

## Acknowledgments

This project is built using Django, Django Rest Framework, and DRF Spectacular. Special thanks to the contributors and the open-source community.

**Note:** Ensure that the necessary configurations and settings are adjusted according to your deployment environment.

Feel free to explore and extend this project for your blogging needs!
