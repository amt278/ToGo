# TODO API with Gin (Go)

A simple RESTful API for managing a list of TODO items, built using the [Gin](https://github.com/gin-gonic/gin) web framework in Go.

## Features

- Get all TODO items
- Add a new TODO item
- Get a TODO item by ID
- Toggle the completion status of a TODO item

## Getting Started

### Prerequisites

- Go installed (version 1.18+ recommended)
- Git (optional, if cloning the repository)

### Installation

1. Clone the repository or copy the code into a file named `main.go`:

   ```bash
   git clone https://github.com/amt278/ToGo.git
   cd ToGo
   ```

2. Initialize Go modules (if not already):

   ```bash
   go mod init todo-api
   ```

3. Install dependencies:

   ```bash
   go get github.com/gin-gonic/gin
   ```

4. Run the server:

   ```bash
   go run main.go
   ```

5. Server will start at `http://localhost:5000`

## API Endpoints

### Get All TODOs

- **URL:** `GET /todos`
- **Response:** List of TODO items

### Add a TODO

- **URL:** `POST /todos`
- **Request Body:**
  ```json
  {
    "id": "4",
    "item": "new task",
    "completed": false
  }
  ```
- **Response:** Newly added TODO item

### Get TODO by ID

- **URL:** `GET /todos/:id`
- **Response:** TODO item with matching ID

### Toggle Completion

- **URL:** `PATCH /todos/:id`
- **Response:** TODO item with toggled `completed` status

## Example

```bash
curl http://localhost:5000/todos
```
