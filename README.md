##  Build a Kubernetes Cluster Locally with Minikube

This project demonstrates how to set up a local Kubernetes cluster using **Minikube**, deploy an **NGINX web server**, and manage the application using `kubectl`. The entire setup is then version-controlled and pushed to GitHub.

---

## 🚀 Project Objectives

- Set up Kubernetes cluster locally using Minikube  
- Deploy a sample NGINX web application  
- Expose the deployment via a Kubernetes Service  
- Access the application via browser  
- Push the entire setup to GitHub for version control

---

## 🧰 Tools Used

- [Minikube](https://minikube.sigs.k8s.io/docs/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Docker](https://www.docker.com/products/docker-desktop/)
- Git & GitHub

---

## 📁 Project Structure
kubernetes-nginx-demo/
│
├── deployment.yaml # Defines NGINX Deployment
├── service.yaml # Exposes NGINX using NodePort Service

---

## 🛠️ Setup Instructions

### 1. Install Prerequisites

- Docker Desktop (enable Kubernetes if possible)
- Install Minikube:  
  https://minikube.sigs.k8s.io/docs/start/
- Install kubectl:  
  https://kubernetes.io/docs/tasks/tools/

> ✅ Tip: Use `choco install minikube kubernetes-cli` if using Windows with Chocolatey.

---

### 2. Start Minikube
- Copy
- minikube start
- Wait for it to set up the cluster and show that the node is in Ready status.

## 3. Create Kubernetes YAML Files
- deployment.yaml
- service.yaml

## 4. Apply the Files to Your Cluster
- Copy
- kubectl apply -f deployment.yaml
- kubectl apply -f service.yaml

## 5. Verify the Setup
- Copy
- kubectl get pods
- kubectl get services

## 6. Access the Application
- Copy
- minikube service nginx-service
- This command will open the NGINX welcome page in your default browser.

## 💾 Push Project to GitHub
- Step-by-Step
- Copy
- git init
- git add .
- git commit -m "Initial commit - Kubernetes NGINX deployment"
- git branch -M main
- git remote add origin https://github.com/your-username/kubernetes-nginx-app.git
- git push -u origin main

## ✅ Outcome
- Successfully deployed NGINX using Kubernetes locally

- Verified deployment and service

- Project pushed to GitHub for version control
