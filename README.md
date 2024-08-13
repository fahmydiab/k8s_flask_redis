## 1. Setup Overview
Web Application: Python Flask App
Database: Redis with persistent storage
Kubernetes Components: Namespace, StatefulSet for Redis, Deployment for Flask, Services for both.
## 2. Step-by-Step Instructions
Step 1: Create the Namespace
Create a namespace called web-db-example to organize your resources.
- "kubectl create namespace web-db-example"

## Step 2: Deploy the Redis Database using StatefulSet
Create a StatefulSet for Redis with persistent storage.

- Create a PersistentVolumeClaim (PVC) for Redis
- Create the StatefulSet for Redis
- Apply the Redis StatefulSet:
"kubectl apply -f redis-statefulset.yaml"

Step 3: Deploy the Flask Web Application
Create a Deployment for the Flask application.

- Create a Deployment for Flask
- Apply the Flask Deployment
  "kubectl apply -f flask-deployment.yaml"

## Step 4: Create Services for Redis and Flask
Expose both the Redis database and the Flask application via Kubernetes Services.

- Create a Service for Redis
- Create a Service for Flask
- Apply the Services:

"kubectl apply -f redis-service.yaml
kubectl apply -f flask-service.yaml"


