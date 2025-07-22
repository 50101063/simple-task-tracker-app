# Integration Documentation

This folder contains all the necessary files and documentation to run the Simple Task Tracker application in a fully integrated, containerized environment.

## Overview

The integration is managed using Docker and Docker Compose. This approach ensures that the frontend, backend, and any other required services run in isolated, consistent, and reproducible environments.

-   **`docker-compose.yml`**: The main orchestration file that defines and configures the `frontend` and `backend` services.
-   **`backend/Dockerfile`**: The recipe for building the Docker image for the Flask backend application.
-   **`frontend/Dockerfile`**: The recipe for building the Docker image for the Vue.js frontend application.

## Prerequisites

-   Docker
-   Docker Compose

## How to Run the Integrated System

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/50101063/simple-task-tracker-app.git
    cd simple-task-tracker-app
    ```

2.  **Build and run the services using Docker Compose:**
    ```bash
    docker-compose up --build
    ```

    This command will:
    -   Build the Docker images for both the `frontend` and `backend` services based on their respective `Dockerfile`s.
    -   Start the containers for both services.
    -   Network the services together so they can communicate.

3.  **Access the application:**
    -   The **Frontend** will be available at `http://localhost:8080`.
    -   The **Backend API** will be available at `http://localhost:5000`.

4.  **Stopping the application:**
    -   To stop the running containers, press `Ctrl+C` in the terminal where `docker-compose` is running, or run the following command from the project root in another terminal:
    ```bash
    docker-compose down
    ```
