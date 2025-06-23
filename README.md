# Blogging API

A simple blogging platform API written in Go, designed to provide basic CRUD and search operations for blog posts. This project uses the Gorilla Mux router and includes rate-limiting middleware and caching mechanisms.

## Features

- Add, view, update, and delete blog posts
- Search blog posts by term
- RESTful API endpoints
- Middleware for rate limiting and caching
- Docker and Docker Compose support for easy deployment

## Endpoints

| Method | Endpoint             | Description                |
|--------|----------------------|----------------------------|
| PUT    | `/add`               | Add a new blog post        |
| DELETE | `/delete/{id}`       | Delete a blog post         |
| GET    | `/view/{id}`         | View a specific blog post  |
| GET    | `/view/` or `/view`  | View all blog posts        |
| POST   | `/update/{id}`       | Update a blog post         |
| POST   | `/search/{term}`     | Search posts by term       |

## Getting Started

### Prerequisites

- [Go](https://golang.org/)
- [Docker](https://www.docker.com/) (optional)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Prateesh94/blogging-api.git
   cd blogging-api
   ```

2. Run the API:
   ```bash
   go run main.go
   ```

3. Or use Docker Compose:
   ```bash
   docker-compose up --build
   ```

The API will be available at `http://localhost:8080`

## Project Structure

```
.
├── blogops/           # Blog operations (handlers, logic)
├── clientandcache/    # Middleware for rate limiting and caching
├── main.go            # API entry point
├── go.mod, go.sum     # Go modules
├── Dockerfile         # Docker support
├── docker-compose.yml # Docker Compose config
```

## Dependencies

- [Gorilla Mux](https://github.com/gorilla/mux)

---

*Built and maintained by Prateesh94*