# Note-Taking Application RESTful API

This repository contains the implementation of a simple note-taking application's RESTful API using Django and Django REST framework. The API allows users to perform basic CRUD operations (Create, Read, Update, Delete) on notes.

## Table of Contents

1. [Features](#features)
2. [Endpoints](#endpoints)
3. [Data Model](#data-model)
4. [Validation](#validation)
5. [Error Handling](#error-handling)
6. [Testing](#testing)
7. [Setup and Installation](#setup-and-installation)
8. [Documentation](#documentation)

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

Follow the steps in the [Build CRUD API with Django REST framework](https://codevoweb.com/build-crud-api-with-django-rest-framework/) article to set up and run the Django CRUD API locally.

## Documentation

For detailed information on each API endpoint, refer to the documentation in the [Build CRUD API with Django REST framework](https://codevoweb.com/build-crud-api-with-django-rest-framework/) article. The documentation provides examples and usage guidelines for interacting with the API.

Feel free to explore, contribute, and enhance this simple note-taking application's RESTful API!