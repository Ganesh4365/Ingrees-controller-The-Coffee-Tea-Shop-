# ☕ Coffee & Tea: Intelligent Path-Based Routing
> **Centralized Traffic Management & Cost Optimization in Kubernetes**

![Architecture Diagram](./your-imag<img width="2752" height="1536" alt="unnamed (1)" src="https://github.com/user-attachments/assets/6206679e-37d6-4130-8307-4b3f4e5c4c21" />
e-link.png)

## 🌟 Project Overview
This project implements a **Kubernetes NGINX Ingress Controller** to manage microservices via path-based routing. By replacing multiple expensive cloud Load Balancers with a single entry point, we achieve a cost-effective, high-availability architecture.

---

## 🏗️ Architecture Design
The Ingress Controller acts as a reverse proxy, routing external clients to the appropriate internal service based on defined rules.

| External Path | Target Service | Logic Applied |
| :--- | :--- | :--- |
| `://domain.com` | `coffee-service` | Prefix matching -> Coffee Pods |
| `://domain.com` | `tea-service` | Prefix matching -> Tea Pods |

---

## 🚀 Deployment Guide

### 1. Create the Applications & Services
Deploy the Coffee and Tea microservices along with their internal ClusterIP services:
```bash
kubectl apply -f shop.yaml
