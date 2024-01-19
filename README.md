
# Banking Web Application

## Overview

This is a full-stack web application for managing user accounts, transactions, and authentication in a banking context. The application is built using a microservices architecture, with Nest.js for the backend, GraphQL for communication between services, Next.js for the frontend, and Next UI for styling.

## Features

- **Microservices Architecture**: The application is divided into several microservices to handle different aspects of banking functionality.
  - **Account Service**: Manages user accounts, balances, and transactions.
  - **Authentication Service**: Handles user authentication and authorization.
  - **Transaction Service**: Manages transaction history.
  - **Frontend Service**: Next.js application that interacts with the microservices.

- **GraphQL**: The services communicate with each other using GraphQL, providing a flexible and efficient way to query and mutate data.

- **Next UI Styling**: Styling for the frontend is implemented using Next UI, providing a clean and responsive user interface.

## Technologies Used

- **Backend**:
  - Nest.js
  - GraphQL
  - Prisma for database access
  - JWT for authentication

- **Frontend**:
  - Next.js
  - Next UI for styling
  - GraphQL for data fetching

## Prerequisites

- Node.js and npm installed
- Docker for running PostgreSQL database in a container

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/banking-app.git
   cd banking-app
   ```

2. **Install Dependencies:**
   ```bash
   # Install backend dependencies
   cd backend
   npm install

   # Install frontend dependencies
   cd ../frontend
   npm install
   ```

3. **Setup PostgreSQL Database:**
   - Create a `docker-compose.yml` file (see provided example).
   - Run `docker-compose up dev-db -d` to start the PostgreSQL container.

4. **Configure Microservices:**
   - Update environment variables in each microservice's `.env` file.

5. **Run the Application:**
   ```bash
   # Run each microservice separately
   cd backend/auth-service
   npm run start:dev

   cd backend/account-service
   npm run start:dev

   cd backend/transaction-service
   npm run start:dev

   cd frontend
   npm run dev
   ```

6. **Access the Application:**
   - Open your browser and go to `http://localhost:3000` to access the Next.js application.

## Contributing

If you would like to contribute to the development of this application, please follow the guidelines in the [CONTRIBUTING.md](CONTRIBUTING.md) file.

## License

This project is licensed under the [MIT License](LICENSE).

