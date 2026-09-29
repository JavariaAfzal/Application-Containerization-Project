# Application Containerization Project

## Overview

This project was developed as part of the Progree DevOps Internship Task 2: Application Containerization & Asset Optimization.

The objective is to build a modular and reliable container environment for a Flask web application using Docker.

##Technologies Used

1. Python
2. Flask
3. Docker
4. Docker Multi-Stage Builds
5. Docker Environment Variables
## Task 2 Requirements Completed

1. Multi-stage Dockerfile
2. Optimized Docker runtime image
3. Runtime environment variable configuration
4. Functional container port routing
5. Successful Docker image build
6. Successful container execution
7. Application verification through browser
## Project Structure

```text
Application-Containerization-Project/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── .dockerignore
├── .env.example
└── README.md

Application:-

The application is a simple Flask web application that runs on port 5000 inside the container.

The application message can be configured using the APP_MESSAGE environment variable.

Docker Multi-Stage Build

The Dockerfile uses two stages:

1.Builder Stage – installs the required Python dependencies.
2.Runtime Stage – creates the final lightweight application image and copies only the required dependencies and application files.

This helps keep the final runtime image cleaner and avoids unnecessary build files.

Environment Configuration:-

The application uses the following environment variable:

APP_MESSAGE
Example:
APP_MESSAGE=Task 2 Environment Variable is working!
The .env.example file provides a configuration template, while environment values can be supplied at container runtime.

Port Mapping

The Flask application listens on container port 5000.

Example Docker port mapping:
Host Port 5002 → Container Port 5000
The application was successfully tested through:
http://localhost:5002

Docker Image:-
The Docker image was successfully built and tested using:
docker build -t application-containerization:3.0 .

Final image details:
Disk Usage: 183 MB
Content Size: 44.7 MB
Verification

The container was successfully verified using:
docker ps

The running container showed:
0.0.0.0:5002->5000/tcp

Internship

Program: Progree DevOps Internship
Task: Task 2 – Application Containerization & Asset Optimization
Domain: DevOps
