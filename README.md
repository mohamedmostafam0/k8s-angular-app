# Full-Stack Application with Docker and Kubernetes

This project demonstrates a full-stack application with a **frontend**, **backend**, and **database**, orchestrated using **Docker Compose** for local development and **Kubernetes** for deployment. The application consists of a frontend service, a backend API, and a MySQL database.

---

## Project Structure

### Docker Compose Setup
- **Frontend**: Serves the user interface and communicates with the backend API.
- **Backend**: Provides the API for the frontend and interacts with the database.
- **Database**: MySQL database for persistent data storage.

### Kubernetes Setup
- **Persistent Volume (PV)**: Manages storage for the MySQL database.
- **Persistent Volume Claim (PVC)**: Requests storage from the PV.
- **Pods**: Deployments for the frontend and backend services.
- **Services**: Exposes the frontend and backend to the network.
- **Ingress**: Manages external access to the frontend service.

---

## File Overview

### Docker Compose (`docker-compose.yaml`)
- Defines three services: `frontend`, `backend`, and `db`.
- Configures environment variables, ports, and dependencies.

### Kubernetes Manifests (`k8s/`)
- **PV.yaml**: Defines a Persistent Volume for MySQL data.
- **PVC.yaml**: Claims storage from the Persistent Volume.
- **backend-pod.yaml**: Defines the backend pod with environment variables.
- **backend-service.yaml**: Exposes the backend service on port 3000.
- **frontend-pod.yaml**: Defines the frontend pod with environment variables.
- **frontend-service.yaml**: Exposes the frontend service on port 80.
- **ingress.yaml**: Configures an Ingress resource to route traffic to the frontend.

---

## Setup Instructions

### Prerequisites
- **Docker** and **Docker Compose** installed.
- **Kubernetes** cluster (e.g., Minikube, Kind, or a cloud provider).
- **kubectl** configured to interact with your Kubernetes cluster.

### Running with Docker Compose
1. Clone the repository:
   ```bash
   git clone https://github.com/mohamedmostafam0/k8s-angular-app.git
   cd k8s-angular-app
2. Build and start the services:
   ```bash
   docker-compose up --build
   ```
4. Access the Application

### Running with Docker Compose   
- **Frontend**: [http://localhost:80](http://localhost:80)
- **Backend API**: [http://localhost:3000](http://localhost:3000)

