# Day 7 - Full Stack Docker Project with CI Pipeline

This project demonstrates how to containerize a full-stack application using Docker and manage it using Docker Compose. It also includes a GitHub Actions CI pipeline to automate Docker builds and pushes to Docker Hub.

## ✅ Project Highlights

### 🔧 Frontend
- Developed using **React** (`react@19.1.0`)
- Resolved vulnerabilities using `npm audit fix --force`
- Dockerized with `Dockerfile`
- Image pushed to Docker Hub:
  [`sanjitheu/full-stack-frontend`](https://hub.docker.com/r/sanjitheu/full-stack-frontend)

### ⚙️ Backend
- Built with **Node.js**
- Dockerized using a separate `Dockerfile`
- Image pushed to Docker Hub:
  [`sanjitheu/full-stack-backend`](https://hub.docker.com/r/sanjitheu/full-stack-backend)

### 📦 Docker Compose
- Orchestrates both frontend and backend containers
- Uses `container_name`, `restart` policy, and port mappings
- Simplifies the process of launching the entire stack

### 🔄 CI/CD Pipeline
- Implemented with **GitHub Actions**
- Automatically:
  - Builds frontend and backend images on push to `main`
  - Pushes the images to Docker Hub using stored secrets

CI Workflow: `.github/workflows/docker-build-push.yml`

---

## 📂 Project Structure

/day7-task-docker/
│
├── frontend/ # React frontend
│ └── Dockerfile
│
├── backend/ # Node.js backend
│ └── Dockerfile
│
├── docker-compose.yml # Docker Compose configuration
├── .github/
│ └── workflows/
│ └── docker-build-push.yml # CI pipeline
