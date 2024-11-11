# Task Manager

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Contributions](#contributions)
- [License](#license)

## Overview
This project is a PHP-based Task Management System designed to help users manage their tasks. It provides functionality for user registration, login, and task management. Users can create, update, delete, and assign tasks to others. The system is built with a simple PHP architecture and renders HTML views for user interaction.

### Features
- **User Registration and Authentication**: Users can register, log in, and manage their sessions.
- **Task Management**: Users can create, view, update, and delete tasks.
- **Task Assignment**: Users can assign tasks to other users.
- **Task Viewing**: Users can view a list of their tasks and the details of each task.
- **Password Change**: Users can change their password.

## Usage
1. **Setup and Deployment**:
    - Clone the repository to your local machine.
    - Ensure you have PHP 8.3+ installed.
    - Run `composer install` to install the required dependencies.
    - Set up a local database for storing users and tasks (e.g., MySQL or PostgreSQL).
    - Configure the database settings in the `src/Database/Database.php` file.
    - Run the application using your web server (e.g., Apache, Nginx, or PHP's built-in server).

2. **Access the Application**:
    - The application can be accessed locally at `http://localhost:8000` or the configured address.

3. **Interacting with the Application**:
    - **GET** `/register`: Retrieve the registration page.
    - **POST** `/register`: Register a new user.
    - **GET** `/login`: Retrieve the login page.
    - **POST** `/login`: Log in with the user credentials.
    - **GET** `/tasks`: View a list of tasks.
    - **POST** `/tasks`: Create a new task.
    - **GET** `/tasks/{id}`: View a specific task by its ID.
    - **PUT** `/tasks/{id}`: Update an existing task by its ID.
    - **DELETE** `/tasks/{id}`: Delete a task by its ID.
    - **GET** `/change-password`: Retrieve the password change page.
    - **POST** `/change-password`: Change the user password.

## File Structure
- `public/`: Publicly accessible files for the project.
    - `index.php`: Main entry point for the application, where routing and request handling occur.

- `src/`: PHP source files for application logic.
    - `Controllers/`: Controllers for handling user requests and interactions with models.
        - `AuthController.php`: Controller for user registration, login, and authentication.
        - `TaskController.php`: Controller for handling task management functionality.
    - `Core/`: Core classes for routing and database interaction.
        - `Router.php`: Router class for handling HTTP requests.
    - `Database/`: Contains database-related functionality.
        - `Database.php`: Database connection and query handling class.
    - `Models/`: Contains model classes for user and task entities.
        - `Task.php`: Task model class for task-related operations.
        - `User.php`: User model class for user-related operations.
    - `Service/`: Contains service classes for handling business logic.
        - `TaskService.php`: Service class for task-related business logic.
        - `UserService.php`: Service class for user-related business logic.
    - `Views/`: Contains `.php` files for rendering HTML templates and forms.
        - `change-password.php`: View for the change password form.
        - `login.php`: View for the login form.
        - `register.php`: View for the registration form.
        - `tasks.php`: View for displaying the list of tasks.

- `composer.json`: Composer configuration file for managing dependencies.

## Contributions
Contributions, feedback, and suggestions are welcome. If you have any improvements or find issues, please submit a pull request or open an issue.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
