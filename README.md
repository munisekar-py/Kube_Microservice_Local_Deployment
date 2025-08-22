# Kube_Microservice_Local_Deployment
Deploy a microservices application on Kubernetes using Minikube / Docker  ensuring proper service communication and configuration.


### 🛠️  Tech Stack

* **Node.js + Express** – Service implementation

* **Docker** – Containerization

* **Docker Compose** – Local service orchestration

* **Kubernetes (kubectl)** – Container orchestration

### 📂 Project Structure

<img width="310" height="500" alt="image" src="https://github.com/user-attachments/assets/d5a01ce4-0094-46ca-a236-083e468ea52e" />


### 🛒 Microservices E-Commerce Project

This project is a **Node.js microservices-based application** that demonstrates containerization and orchestration using **Docker**, **Docker Compose**, and **Kubernetes**.  

It includes the following services:
- **Gateway Service** – API Gateway that routes requests to other services
- **User Service** – Manages user-related operations
- **Product Service** – Manages product catalog
- **Order Service** – Manages order creation and tracking

---
**Docker- Desktop as Kube Provider**
```
 ⚡munish ❯❯ kubectl  config get-contexts
CURRENT   NAME             CLUSTER          AUTHINFO         NAMESPACE
*         docker-desktop   docker-desktop   docker-desktop   

```
---
### Basic Kubernetes Deployment 
**munish:  kubectl apply -f k8s/**
```
deployment.apps/gateway-service created
service/gateway-service created
deployment.apps/order-service created
service/order-service created
deployment.apps/product-service created
service/product-service created
deployment.apps/user-service created
service/user-service created

```
---
 **munish ❯❯ kubectl get pods**
```
NAME                               READY   STATUS    RESTARTS   AGE
gateway-service-7bf654fc96-c4w6p   1/1     Running   0          57s
order-service-bd4884b48-zbnln      1/1     Running   0          57s
product-service-86d78755ff-j7dfz   1/1     Running   0          57s
user-service-7445665595-ds69v      1/1     Running   0          57s
```

---
**munish ❯❯ kubectl get svc**
```
NAME              TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
gateway-service   NodePort    10.111.244.65    <none>        3003:30083/TCP   116s
kubernetes        ClusterIP   10.96.0.1        <none>        443/TCP          15d
order-service     ClusterIP   10.97.142.211    <none>        3002/TCP         116s
product-service   ClusterIP   10.104.194.98    <none>        3001/TCP         116s
user-service      ClusterIP   10.103.158.139   <none>        3000/TCP         116s
````

---

**munish ❯❯ kubectl get deployments**
```
NAME              READY   UP-TO-DATE   AVAILABLE   AGE
gateway-service   1/1     1            1           33m
order-service     1/1     1            1           33m
product-service   1/1     1            1           33m
user-service      1/1     1            1           33m
```
**⚡munish ❯❯ kubectl get all**

<img width="954" height="591" alt="Screenshot from 2025-08-22 15-18-52" src="https://github.com/user-attachments/assets/fdb04fe4-1934-44a5-952e-ef3cf0946af9" />

### Testing
```
⚡munish ❯❯ curl http://localhost:30083/api/users

[{"id":1,"name":"John Doe"},{"id":2,"name":"Jane Smith"}]

 ⚡munish ❯❯ curl http://localhost:30083/api/products
 
[{"id":1,"name":"Laptop","price":999},{"id":2,"name":"Phone","price":699}]
```
---

<img width="308" height="262" alt="image" src="https://github.com/user-attachments/assets/c87a8f4a-7a73-4170-809f-0d3cb8bdd39b" />
