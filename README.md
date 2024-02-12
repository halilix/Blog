# Blog API

This project constitutes a simple RESTful API for managing blog posts and comments.

## Table of Contents

- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Authentication](#authentication)
- [Contributing](#contributing)

## Introduction

The Blog API is designed to facilitate the management of blog posts and associated comments. It provides endpoints for creating, reading, updating, and deleting both posts and comments. The API is built using ASP.NET Core and Entity Framework Core for database interactions.

## Technologies Used

- C#
- ASP.NET Core
- Entity Framework Core
- Microsoft SQL Server (assumed based on DbContext usage)
- JSON Web Tokens (JWT) for authentication
- Microsoft.AspNetCore.Authentication.JwtBearer for JWT authentication

## Installation

1. Clone the repository to your local machine.
2. Open the solution file (`Blog.sln`) in Visual Studio or your preferred C# IDE.
3. Build the solution to restore dependencies.
4. Update the connection string in the `appsettings.json` file to point to your SQL Server instance.
5. Run the database migrations to create the necessary tables:

dotnet ef database update

6. Start the application.

## Usage

Once the application is running, you can interact with it using HTTP requests to the provided endpoints. You may use tools like Postman or curl to make requests.

## Endpoints

The API exposes the following endpoints:

- `GET /api/posts`: Retrieve all posts.
- `GET /api/posts/{id}`: Retrieve a specific post along with its comments.
- `POST /api/posts`: Create a new post.
- `PUT /api/posts/{id}`: Update an existing post.
- `DELETE /api/posts/{id}`: Delete an existing post.
- `GET /api/comments`: Retrieve all comments.
- `POST /api/comments`: Create a new comment.
- `PUT /api/comments/{id}`: Update an existing comment.
- `DELETE /api/comments/{id}`: Delete an existing comment.

## Authentication

The API requires authentication to access its endpoints. It utilizes JWT (JSON Web Tokens) for authentication. To access protected endpoints, clients must include a valid JWT token in the request header.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with your changes.
