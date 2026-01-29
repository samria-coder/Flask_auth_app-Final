# Flask Authentication App (Docker + Kubernetes Deployment)

This project is a simple authentication web application built using **Python Flask**.  
It supports **user registration** and **login** using a **SQLite/MySQL database**.  
The application is **containerized using Docker**, published to **DockerHub**, and deployed on **Kubernetes** (Minikube or AWS EKS).

This project demonstrates a full development-to-deployment workflow:
- Flask backend development  
- Database integration  
- GitHub version control  
- Docker containerization  
- DockerHub image publishing  
- Kubernetes deployment (`kubectl`)  
- LoadBalancer service exposure  

---

## 🚀 Features

- User Registration  
- User Login  
- SQLite or MySQL backend  
- Easy-to-run Docker container  
- Kubernetes-ready deployment files  
- Clean and simple project structure  

---

## 📁 Project Structure
flask-auth-app/
│── app.py
│── requirements.txt
│── Dockerfile
│── k8s-deployment.yaml
│── k8s-service.yaml
│── templates/
│── static/
│── database.db (if using SQLite)


 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<your-username>/flask-auth-app.git
cd flask-auth-app

Run Locally (Without Docker)
pip install -r requirements.txt
python app.py

App runs at:
http://localhost:5000

Docker Instructions
Build Image
docker build -t flask-auth-app .

Run Container
docker run -p 5000:5000 flask-auth-app

Push to DockerHub
docker tag flask-auth-app <dockerhub-username>/flask-auth-app:v1
docker push <dockerhub-username>/flask-auth-app:v1

Kubernetes Deployment
Apply Deployment
kubectl apply -f k8s-deployment.yaml

Apply Service
kubectl apply -f k8s-service.yaml

Get Service URL
Minikube:
minikube service flask-auth-service
EKS:
kubectl get svc flask-auth-service

Testing the App
Open the browser
Register a user
Log in using the created credentials

Technologies Used
Python Flask
SQLite / MySQL
Docker
DockerHub
Kubernetes
GitHub
