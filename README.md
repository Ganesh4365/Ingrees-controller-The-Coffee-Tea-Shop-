# Ingrees-controller-The-Coffee-Tea-Shop-
Dual-App Router


# ☕ Coffee & Tea: Intelligent Path-Based Routing
> **Centralized Traffic Management & Cost Optimization in Kubernetes**

<p align="center">
  <img src="./routing-diagram.png" alt="Kubernetes Ingr![Uploading unnamed (1).png…]()
ess Architecture" width="700">
</p>

![K8s](https://img.shields.io)
![Nginx](https://img.shields.io)
![Traffic](https://img.shields.io)

## 🌟 Project Overview
This project implements a **Kubernetes NGINX Ingress Controller** to manage microservices via path-based routing. By replacing multiple expensive cloud Load Balancers with a single entry point, we achieve a cost-effective, high-availability architecture.

### Key Technical Features:
*   **Layer 7 Routing:** Intelligent request matching based on URL suffixes (`/coffee` or `/tea`).
*   **Endpoint Discovery:** Automated pod identification via the Kubernetes API.
*   **Path Rewriting:** Utilizes NGINX annotations to ensure backend services receive clean requests.
*   **Resource Efficiency:** Optimal traffic management in multi-node clusters.

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


