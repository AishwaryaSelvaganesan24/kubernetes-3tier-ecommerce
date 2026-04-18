# 🛒 3-Tier E-commerce Application on Kubernetes

## 📌 Project Overview

This project demonstrates the deployment of a **3-tier application architecture** using Kubernetes (Minikube).

The application is divided into:

* **Frontend** (NGINX + UI)
* **Backend** (API service)
* **Database** (MySQL)

The goal of this project is to understand real-world Kubernetes architecture, internal networking, and deployment practices.

---

## 🧱 Architecture

```
User (Browser)
      ↓
Frontend (NGINX)
      ↓  /api
Backend Service (ClusterIP)
      ↓
Backend Pod
      ↓
MySQL Database
```

---

## ⚙️ Tech Stack

* Kubernetes (Minikube)
* Docker
* NGINX (Frontend & Reverse Proxy)
* MySQL (Database)
* YAML (Kubernetes manifests)

---

## 🚀 Features

* 3-tier architecture deployment on Kubernetes
* Kubernetes **Deployments** and **Services**
* Secure credential management using **Secrets**
* Configuration management using **ConfigMaps**
* Internal service communication using Kubernetes DNS
* NGINX reverse proxy setup to route frontend → backend
* Hands-on debugging of real-world issues

---

## 📂 Project Structure

```
k8s-3tier-ecommerce/
│
├── frontend/
│   ├── frontend-deployment.yaml
│   ├── frontend-service.yaml
│   ├── frontend-configmap.yaml
│   └── frontend-nginx-config.yaml
│
├── backend/
│   ├── backend-deployment.yaml
│   └── backend-service.yaml
│
├── database/
│   ├── mysql-deployment.yaml
│   ├── mysql-service.yaml
│   └── mysql-secret.yaml
│
├── namespace.yaml
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Start Minikube

```
minikube start
```

### 2. Apply Kubernetes Resources

```
kubectl apply -f namespace.yaml

kubectl apply -f database/
kubectl apply -f backend/
kubectl apply -f frontend/
```

---

## 🌐 Access the Application

```
minikube service frontend -n ecommerce
```

This will open the application in your browser.

---

## 🧠 Key Learnings

* Understanding Kubernetes architecture (Pods, Deployments, Services)
* Service discovery using Kubernetes DNS
* Managing sensitive data using Secrets
* Using ConfigMaps for configuration and UI
* Implementing NGINX reverse proxy inside Kubernetes
* Debugging issues like:

  * Pod failures
  * Service misconfiguration
  * Port mismatch
  * Namespace communication issues
  * ConfigMap mounting errors

---

## 🚧 Future Improvements

* Implement real backend logic (Node.js / Spring Boot)
* Connect backend with MySQL database
* Build interactive frontend (React or advanced UI)
* Deploy on cloud using AWS EKS
* Add CI/CD pipeline

---

## 📌 Author

**Aishwarya Selvaganesan**

---

## ⭐ Notes

This project focuses on **infrastructure and architecture setup** rather than full application logic, making it a strong foundation for DevOps and Cloud Engineering roles.
