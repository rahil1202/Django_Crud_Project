# Django CRUD RESTful API

This repository contains the implementation of a simple note-taking application's RESTful API using Django and Django REST framework. The API allows users to perform basic CRUD operations (Create, Read, Update, Delete) on notes.

## Table of Contents

1. [Features](#features)
2. [Endpoints](#endpoints)
3. [Data Model](#data-model)
4. [Validation](#validation)
5. [Error Handling](#error-handling)
6. [Testing](#testing)
7. [Setup and Installation](#setup-and-installation)
8. [Usage](#usage)
9. [Documentation](#documentation)
10. [Contributing](#contributing)
11. [License](#license)

## Features

- User authentication with login and signup endpoints.
- Create, read, update, and delete notes.
- Share notes with other users.
- Retrieve version history of a note.

## Endpoints

- **POST /login:** Create a user login view.
- **POST /signup:** Create a single user sign up view.
- **POST /notes/create:** Create a new note.
- **GET /notes/{id}:** Retrieve a specific note by its ID.
- **POST /notes/share:** Share the note with other users.
- **PUT /notes/{id}:** Update an existing note.
- **GET /notes/version-history/{id}:** Get all the changes associated with the note.

## Data Model

The application uses an efficient database schema that supports user information and note details.

- **User Model:**
  - `id` (Auto-generated)
  - `username` (String, unique)
  - `password` (String)

- **Note Model:**
  - `id` (Auto-generated)
  - `title` (String)
  - `content` (Text)
  - `created_at` (DateTime)
  - `updated_at` (DateTime)
  - `created_by` (Foreign key to User)
  - `shared_with` (Many-to-Many relationship with User)

## Validation

Basic input validation is implemented for creating and updating notes. Required fields are validated, and appropriate data types are enforced.

## Error Handling

The API handles errors gracefully and returns meaningful error responses with appropriate HTTP status codes for better user experience.

## Testing

Unit tests are provided to ensure the functionality and integrity of the API endpoints. You can run tests using Django's testing framework.

## Setup and Installation

To set up and run the Django CRUD API locally, follow these steps:

### Prerequisites

- Make sure you have Python installed on your system. You can download it from [python.org](https://www.python.org/downloads/).

### Clone the Repository

```bash
git clone https://github.com/your-username/note-taking-api.git
cd note-taking-api
```

### Create a Virtual Environment

```bash
python -m venv venv
```

### Activate the Virtual Environment

- On Windows:

```bash
venv\Scripts\activate
```

- On macOS/Linux:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### Create a Superuser (Optional)

If you want to access the Django admin panel:

```bash
python manage.py createsuperuser
```

Follow the prompts to create a superuser (admin) account.

### Start the Development Server

```bash
python manage.py runserver
```

The API will be accessible at [http://localhost:8000/](http://localhost:8000/).

### Accessing Django Admin Panel

If you created a superuser, you can access the Django admin panel at [http://localhost:8000/admin/](http://localhost:8000/admin/) and log in with the superuser credentials.


## Contributing

Feel free to explore, contribute, and enhance this simple note-taking application's RESTful API! If you encounter any issues, refer to the [Django documentation](https://docs.djangoproject.com/) or the [Django REST framework documentation](https://www.django-rest-framework.org/).

## License

This project is licensed under the [MIT License](LICENSE).