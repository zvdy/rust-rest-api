# Rust Rest Api

This is a simple Rust project that provides a RESTful API for managing users. It uses Postgres as the database and provides endpoints for creating, retrieving, updating, and deleting users.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Docker
- Docker Compose

### Running the Project

1. Clone the repository:

```bash
git clone https://github.com/zvdy/repository.git
cd repository
```

2. Build and run the project using Docker Compose:

```bash
docker-compose build
docker-compose up
```

The server will start at `localhost:8080`.

## Testing the API

You can use `curl` to test the API endpoints.

### Create a User

```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"John Doe","email":"john@example.com"}' http://localhost:8080/users
```

### Retrieve a User

Replace `:id` with the ID of the user you want to retrieve.

```bash
curl -X GET http://localhost:8080/users/:id
```

### Retrieve All Users

```bash
curl -X GET http://localhost:8080/users
```

### Update a User

Replace `:id` with the ID of the user you want to update.

```bash
curl -X PUT -H "Content-Type: application/json" -d '{"name":"Jane Doe","email":"jane@example.com"}' http://localhost:8080/users/:id
```

### Delete a User

Replace `:id` with the ID of the user you want to delete.

```bash
curl -X DELETE http://localhost:8080/users/:id
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.
