# Ticket Reservation System

A simple cinema ticket booking application built with Go and vanilla JavaScript.

## Features
- **Movie Listing**: Browse available movies.
- **Seat Selection**: Interactive seat map with real-time availability.
- **Booking System**: Hold seats for 5 minutes before confirming.
- **My Tickets**: View your booking history.
- **Concurrency Handling**: Prevents double booking of seats.

## Prerequisites
- [Go](https://go.dev/dl/) (version 1.25 or higher)
- Make (optional, for using the Makefile)

## Getting Started

### 1. Install Dependencies
Download the required Go modules:
```bash
make deps
# Or manually:
go mod download
```

### 2. Run the Application
Start the server directly:
```bash
make run
# Or manually:
go run ./cmd/server
```
The server will start at [http://localhost:8080](http://localhost:8080).
The database (`cinema.db`) will be automatically created and seeded with sample data on the first run.

### 3. Build the Application
Compile the binary to `bin/server`:
```bash
make build
# Or manually:
go build -o bin/server ./cmd/server
```

## Cleanup
Remove the binary and the SQLite database:
```bash
make clean
```

## Project Structure
```
.
├── cmd/
│   └── server/       # Application entry point
├── internal/
│   ├── database/     # Database initialization and schema
│   ├── handlers/     # HTTP API handlers
│   └── models/       # Data structures
├── static/           # Frontend assets (HTML, CSS, JS)
├── go.mod            # Go module definition
└── makefile          # Build automation
```
