# Labour Hiring System

This project is a **Labour Hiring System** deployed using **Docker**, **Kubernetes**, and **Jenkins** to automate deployment and management. The system consists of three primary components:

- **Backend**: A Node.js-based server that handles business logic and API requests.
- **Frontend**: A React-based application providing a user interface to interact with the backend.
- **Database**: A MySQL database to store labour hiring-related data.

The project demonstrates how to containerize applications, deploy them on Kubernetes, and automate the entire CI/CD pipeline using Jenkins.

## Tools & Technologies Used

- **Docker**: For containerization of the backend, frontend, and database.
- **Kubernetes**: For orchestration and management of containerized applications (via Minikube).
- **Jenkins**: For automating the CI/CD pipeline.
- **GitHub**: For version control.
- **YAML**: For Kubernetes configurations.
- **MySQL**: For the database service.

## Project Structure

LabourHiringSystem/ ├── backend/ │ ├── Dockerfile │ ├── server.js │ └── package.json ├── frontend/ │ ├── Dockerfile │ ├── package.json │ └── src/ ├── database/ │ └── Dockerfile ├── kubernetes/ │ ├── backend-deployment.yaml │ ├── frontend-deployment.yaml │ └── database-deployment.yaml ├── Jenkinsfile └── README.md


### Backend

The backend is a simple Node.js Express server that listens on port `3000`. It exposes an endpoint `/` that responds with a "Hello, World!" message. It interacts with the database to manage labour hiring data.

- **Dockerfile**: Contains the configuration to containerize the Node.js backend.
- **server.js**: The main application file to handle HTTP requests.
- **package.json**: Defines project dependencies and scripts.

### Frontend

The frontend is a React-based application that communicates with the backend to display hiring information. It is containerized using Docker and runs on port `3000`.

- **Dockerfile**: Configures the containerization of the frontend React app.
- **package.json**: Manages frontend dependencies and build scripts.
- **src/**: Contains the source code for the React application.

### Database

The database is a MySQL container, pre-configured with a root password and a database called `labour_hiring`.

- **Dockerfile**: Configures the MySQL container with environment variables for root password and database name.

### Kubernetes Configurations

The Kubernetes configuration files define the deployments and services for each component:

- **backend-deployment.yaml**: Deploys the backend as a service on Kubernetes.
- **frontend-deployment.yaml**: Deploys the frontend as a service on Kubernetes.
- **database-deployment.yaml**: Deploys the database as a service on Kubernetes.

### Jenkins Pipeline

The Jenkins pipeline automates the build, push, and deploy processes using a `Jenkinsfile`. It builds Docker images for the backend, frontend, and database, pushes them to Docker Hub, and deploys them to the Kubernetes cluster.

## Setup Instructions

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/Ronu010/LabourHiringSystem.git
cd LabourHiringSystem


