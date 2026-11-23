# Node.js Fastify & MongoDB CRUD API

A simple CRUD API built with [Fastify](https://www.fastify.io/) and [MongoDB](https://www.mongodb.com/), designed to manage customer data.

## Features

- **Health Check**: `/v1/health`
- **Get Customers**: Retrieve a list of all customers.
- **Get Customer by ID**: Retrieve a specific customer's details by their unique ID.
- **Create Customer**: Add a new customer to the database.
- **Update Customer**: Update existing customer information.
- **Docker Support**: Easy to run with Docker and Docker Compose.

## Prerequisites

- Node.js (v20.11.0 recommended)
- Docker and Docker Compose

## Getting Started

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd nodejs-fastify-mongodb-crud
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

### Running the Application

#### Using Node.js directly
Ensure you have a running MongoDB instance and set the required environment variables.
```bash
DB_NAME=customers node src/index.js
```

#### Using Docker
Start the infrastructure (MongoDB, etc.) and run the application:
```bash
# Start infrastructure
npm run docker:infra:up

# Start the application
npm run dev
```

### Testing

Run the test suite:
```bash
npm run test
```

## Project Structure

- `src/`: Contains the source code for the API.
- `config/`: Seed files for database initialization.
- `test/`: Test files for the API endpoints.
- `Dockerfile`: Configuration for containerizing the application.
- `docker-compose.yml`: Orchestration for multi-container setup.

## Environment Variables

| Variable | Description | Default |
| --- | --- | --- |
| `DB_NAME` | Name of the MongoDB database | `random-test` |
| `DB_USER` | MongoDB username | `root` |
| `DB_PASSWORD` | MongoDB password | `example` |
| `DB_HOST` | MongoDB host address | `localhost` |
| `DB_PORT` | MongoDB port | `27017` |

## License

Distributed under the MIT License. See `LICENSE` for more information.
