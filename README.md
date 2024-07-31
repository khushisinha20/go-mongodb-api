# Go MongoDB API

This is a simple RESTful API built with Go, Gorilla Mux, and MongoDB. It allows you to manage a watchlist of movies, providing endpoints to create, read, update, and delete movies.

## Prerequisites

- Go 1.16 or later
- MongoDB Atlas account (or a local MongoDB instance)
- Gorilla Mux

## Project Structure
```
├── controller
│   └── controller.go
├── model
│   └── models.go
├── router
│   └── router.go
├── main.go
├── go.mod
└── go.sum
```

## Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/khushisinha20/mongoapi.git
    cd mongoapi
    ```

2. Install the dependencies:

    ```bash
    go mod tidy
    ```

3. Update the MongoDB connection string in `controller/controller.go`:

    ```go
    const connectionString = "your_mongodb_connection_string"
    ```

## Running the API

To start the server, run:

```bash
go run main.go
```

The server will start at `http://localhost:4000`.

## API Endpoints

| Method | Endpoint            | Description             |
|--------|---------------------|-------------------------|
| GET    | /api/movies         | Get all movies          |
| POST   | /api/movie          | Create a new movie      |
| PUT    | /api/movie/{id}     | Mark a movie as watched |
| DELETE | /api/movie/{id}     | Delete a specific movie |
| DELETE | /api/deleteallmovie | Delete all movies       |

## Testing the API
You can test the API using tools like Postman or Thunder Client (an extension for VS Code).