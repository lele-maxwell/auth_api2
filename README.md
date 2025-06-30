# 🚀 Auth API 2 - Kubernetes Deployment

[![Build and Slim Docker Images](https://github.com/lele-maxwell/auth_api2/actions/workflows/docker-ghcr.yml/badge.svg)](https://github.com/lele-maxwell/auth_api2/actions/workflows/docker-ghcr.yml)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-1.28+-326CE5.svg)](https://kubernetes.io/)

A production-ready Kubernetes deployment for a fullstack authentication system with **Rust (Axum)** backend and **React (TypeScript)** frontend.

> 📖 **For detailed authentication features and API documentation, see: [Auth API Repository](https://github.com/lele-maxwell/auth_api.git)**

---

## 📦 Project Structure

```
auth_api2/
├── k8s/                         # Kubernetes manifests
│   ├── backend-deployment.yaml  # Backend deployment configuration
│   ├── frontend-deployment.yaml # Frontend deployment configuration
│   ├── backend-service.yaml     # Backend service configuration
│   ├── frontend-service.yaml    # Frontend service configuration
│   ├── backend-configmap.yaml   # Backend configuration
│   ├── backend-secret.yaml      # Backend secrets
│   └── frontend-configmap.yaml  # Frontend configuration
├── .github/workflows/           # CI/CD pipelines
│   └── docker-ghcr.yml         # Automated Docker builds
├── Dockerfile.backend           # Backend Docker configuration
└── front-end/Dockerfile.frontend # Frontend Docker configuration
```

---

## 🧠 What This Project Demonstrates

- ✅ Kubernetes-native deployment architecture
- ✅ Multi-container application orchestration
- ✅ Automated CI/CD with GitHub Actions
- ✅ Docker image optimization with Docker Slim
- ✅ GitHub Container Registry integration
- ✅ Production-ready K8s manifests
- ✅ ConfigMap and Secret management

---

## 🛠 How to Use

### 1. Clone this repository

```bash
git clone https://github.com/lele-maxwell/auth_api2.git
cd auth_api2
```

### 2. Create Local Kubernetes Cluster (Kind)

```bash
kind create cluster --name auth-cluster
kubectl cluster-info --context kind-auth-cluster
```

### 3. Apply Kubernetes Manifests

```bash
kubectl apply -f k8s/
```

### 4. Verify Deployment

```bash
kubectl get pods
kubectl get services
```

### 5. Access the Application

```bash
# Port forward to access locally
kubectl port-forward svc/auth-frontend-service 8080:80
kubectl port-forward svc/auth-backend-service 3000:8000
```

Access the application at:
- **Frontend**: http://localhost:8080
- **Backend API**: http://10.223.54.148:30080/
- **Swagger UI**: http://10.223.54.148:30080/swagger-ui/

---

## 🛠️ Tech Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Orchestration** | Kubernetes | Container orchestration |
| **CI/CD** | GitHub Actions | Automated builds |
| **Registry** | GitHub Container Registry | Image storage |
| **Optimization** | Docker Slim | Image size reduction |
| **Backend** | Rust + Axum | High-performance API |
| **Frontend** | React + TypeScript | Modern UI |

---

## 🔄 CI/CD Pipeline

The project includes automated CI/CD with GitHub Actions:

- **Automated Builds**: Triggered on main branch pushes
- **Docker Images**: Multi-stage builds with optimization
- **Image Slimming**: Docker Slim integration for reduced sizes
- **Registry Push**: Automatic deployment to GitHub Container Registry

---

## 🧠 My Learning Journey

This project represents my continued growth in infrastructure and Kubernetes deployment. Before this, I started my infrastructure journey with my first Kubernetes deployment:

### 🚀 [Simple Web App with Kubernetes](https://github.com/lele-maxwell/simple-web-app.git)

My first step into Kubernetes was deploying a simple web server using **k3s** and basic manifests. That project demonstrated:
- ✅ Creating a Dockerized web application
- ✅ Writing Kubernetes Deployment and Service manifests  
- ✅ Deploying to a local k3s cluster using `kubectl`
- ✅ Exposing the app using NodePort and accessing via browser

> 💡 **Keep Going!**  
> Every complex infrastructure starts with a simple `kubectl apply`.  
> You're on the right path—keep experimenting, keep learning, and don't be afraid to break things!

---

## ✍️ Author

**Lele Maxwell**

This project marks another milestone in my Kubernetes learning journey, building upon my foundational experience. From simple web apps to fullstack authentication APIs - stay tuned for more!

---

## 🧊 License

This project is open-source and free to use.

---

> Made with by Lele Maxwell
