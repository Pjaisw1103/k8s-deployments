# 🚀 Kubernetes Deployments & Rollout Management

[![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)](#)

Declarative Kubernetes **Deployment** specification for managing scalable, fault-tolerant containerized applications (`Nginx 1.29`) with zero-downtime updates and automated rollbacks.

---

## 📌 Deployment Architecture

- **Deployment Name**: `nginx-deployment`
- **Replicas**: `4` Pod instances
- **Label Selector**: `app: nginx`
- **Container Port**: `80`

---

## 📂 Repository Structure

```text
k8s-deployments/
├── deployment.yaml     # Declarative Deployment manifest
└── README.md           # Repository Documentation
```

---

## 🚀 Usage Guide

### Prerequisites
- Active Kubernetes cluster and configured `kubectl` CLI tool.

### 1. Apply Deployment Manifest

```bash
# Create Deployment
kubectl apply -f deployment.yaml

# Check Deployment status
kubectl get deployments

# Track managed Pods
kubectl get pods -l app=nginx
```

### 2. Rolling Updates & Rollback Commands

```bash
# Perform image update (RollingUpdate)
kubectl set image deployment/nginx-deployment nginx=nginx:alpine

# Track rollout progress
kubectl rollout status deployment/nginx-deployment

# Check rollout revision history
kubectl rollout history deployment/nginx-deployment

# Rollback to previous deployment state
kubectl rollout undo deployment/nginx-deployment
```

### Cleanup

```bash
kubectl delete -f deployment.yaml
```

---

## 👩‍💻 Author

**Priya Jaiswal**  
[GitHub Profile](https://github.com/Pjaisw1103)
