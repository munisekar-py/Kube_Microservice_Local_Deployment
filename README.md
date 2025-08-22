# Kube_Microservice_Local_Deployment
Deploy a microservices application on Kubernetes using Minikube / Docker  ensuring proper service communication and configuration.


### 🛠️  Tech Stack

* **Node.js + Express** – Service implementation

* **Docker** – Containerization

* **Docker Compose** – Local service orchestration

* **Kubernetes (kubectl)** – Container orchestration

### 📂 Project Structure

<img width="310" height="500" alt="image" src="https://github.com/user-attachments/assets/d5a01ce4-0094-46ca-a236-083e468ea52e" />


# 🛒 Microservices E-Commerce Project

This project is a **Node.js microservices-based application** that demonstrates containerization and orchestration using **Docker**, **Docker Compose**, and **Kubernetes**.  

It includes the following services:
- **Gateway Service** – API Gateway that routes requests to other services
- **User Service** – Manages user-related operations
- **Product Service** – Manages product catalog
- **Order Service** – Manages order creation and tracking

---


```
 ⚡munish ❯❯ kubectl apply -f k8s/
 
deployment.apps/gateway-service created
service/gateway-service created
deployment.apps/order-service created
service/order-service created
deployment.apps/product-service created
service/product-service created
deployment.apps/user-service created
service/user-service created

```


<img width="954" height="591" alt="Screenshot from 2025-08-22 15-18-52" src="https://github.com/user-attachments/assets/fdb04fe4-1934-44a5-952e-ef3cf0946af9" />


<img width="748" height="180" alt="Screenshot from 2025-08-22 15-19-19" src="https://github.com/user-attachments/assets/c76e144e-80a2-4805-9a33-0394156928d8" />


<img width="881" height="197" alt="image" src="https://github.com/user-attachments/assets/d7fed941-9c88-4842-8377-d4b499076d60" />
