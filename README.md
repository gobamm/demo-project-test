
# My Node.js Project

This is a Node.js application built with Express. It provides a simple API and is designed to be easily deployable in a Docker container. This project demonstrates best practices for organizing and containerizing a Node.js application.

## Table of Contents
- [Project Structure](#project-structure)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Running in Docker](#running-in-docker)
- [Environment Variables](#environment-variables)
- [Scripts](#scripts)
- [License](#license)

## Project Structure

```
my-nodejs-project/
├── .env               # Environment variables
├── Dockerfile         # Docker configuration
├── .gitignore         # Git ignore file
├── package.json       # Project metadata and dependencies
├── src/               # Source code
│   └── index.js       # Main application file
└── tests/             # Test files
    └── app.test.js    # Example test file
```

## Features

- Basic Express server setup.
- Environment variable configuration using dotenv.
- Dockerfile for containerizing the application.
- Linting with ESLint and optional Jest testing.

## Prerequisites

- [Node.js](https://nodejs.org/) v14 or later
- [Docker](https://www.docker.com/) (optional, for containerization)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/my-nodejs-project.git
   cd my-nodejs-project
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

## Running the Application

1. **Set up environment variables**:
   - Create a `.env` file in the root directory with the following content:
     ```plaintext
     PORT=3000
     ```
   - You can modify the port number as needed.

2. **Run in Development Mode**:
   ```bash
   npm run dev
   ```
   - The application will run at `http://localhost:3000` by default.

3. **Run in Production Mode**:
   ```bash
   npm start
   ```

## Running in Docker

1. **Build the Docker image**:
   ```bash
   docker build -t my-nodejs-app .
   ```

2. **Run the Docker container**:
   ```bash
   docker run -p 3000:3000 my-nodejs-app
   ```
   - The application will be available at `http://localhost:3000`.

## Environment Variables

This project uses environment variables defined in a `.env` file. Below is the main variable used in this project:

- `PORT`: The port on which the server will run (default is 3000).

## Scripts

The following scripts are available in `package.json`:

- **`npm start`**: Runs the application in production mode.
- **`npm run dev`**: Runs the application in development mode with auto-reloading using Nodemon.
- **`npm run lint`**: Runs ESLint to check for coding style issues.
- **`npm test`**: Runs tests with Jest.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
