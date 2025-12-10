# Giftlink Project

## Description

This project is a full-stack web application with a React front-end and a Node.js back-end connected to a MongoDB database. All components are containerized and orchestrated using Kubernetes on IBM Cloud.

The application allows managing gifts with full CRUD (Create, Read, Update, Delete) functionality, featuring a user-friendly interface and a secure RESTful API.

## Technologies Used

- **Front-end:** React
- **Back-end:** Node.js with Express
- **Database:** MongoDB
- **Containerization:** Docker
- **Orchestration:** Kubernetes
- **Deployment:** IBM Cloud Kubernetes Service and IBM Code Engine
- **Version Control:** Git and GitHub

## Project Structure

- `/frontend` — React client code
- `/backend` — Node.js server code
- `/deploy` — Kubernetes configuration files (`deploymongo.yml`, `deployment.yml`, etc.)
- `.env` — environment variables for front-end and back-end

## How to Run the Project

### Prerequisites

- IBM Cloud account configured
- IBM Cloud CLI installed and logged in
- Kubernetes cluster configured on IBM Cloud
- Docker installed (for local builds, if needed)

### Main Steps

1. Build Docker images for the front-end and back-end.
2. Push the images to IBM Cloud Container Registry.
3. Apply Kubernetes deployments for MongoDB, backend, and frontend.
4. Configure environment variables, including URLs and secrets.
5. Access the application via the URL provided by the Kubernetes service or IBM Code Engine.

## Important Environment Variables

- `MONGO_URL` — MongoDB connection URL (e.g., `mongodb://mongodb-service:27017`)
- `JWT_SECRET` — JWT secret key for the backend
- `REACT_APP_BACKEND_URL` — Backend URL used by the React front-end

## Useful Commands

- Check deployments:
- 
```bash
   kubectl get deployments
 
```bash
  Delete an existing deployment:
  kubectl delete deployment <deployment-name>

Commit and push to GitHub:
```bash
  git add .
  git commit -m "Your commit message"
  git push origin main
