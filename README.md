# React-Portfolio-K8s

# 🌐 React Portfolio Website — Production Deployment on Kubernetes

Welcome to the repository for my **React-based portfolio website**, built with modern frontend technologies and deployed using a scalable, cloud-native infrastructure powered by **Docker** and **Kubernetes**.

This project demonstrates how a personal portfolio can be deployed with the same practices used in real-world, production-grade web applications. The deployment process was inspired by [Kastro Kiran’s Zomato App Deployment Tutorial](https://youtu.be/GyoI6-I68aQ).

---

## 🚀 Live Demo

> 🔗 [Add your live deployment link here]  
> *(Optional: You can also add a screenshot or demo GIF here)*

---

## 🧰 Tech Stack

| Technology     | Purpose                              |
|----------------|--------------------------------------|
| React.js       | Frontend user interface              |
| Docker         | Application containerization         |
| Kubernetes     | Orchestration and scaling            |
| NGINX Ingress  | Routing and domain management        |
| ConfigMaps     | Environment-based configuration      |
| Minikube/Cloud | Local or cloud-native deployment     |

---

## 📁 Project Structure

react-portfolio-k8s/
├── client/ # React app source code
│ ├── public/
│ └── src/
├── Dockerfile # Docker build config for React app
├── k8s/ # Kubernetes manifests
│ ├── deployment.yaml
│ ├── service.yaml
│ ├── ingress.yaml
│ └── configmap.yaml
└── README.md

yaml
Copy
Edit

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/react-portfolio-k8s.git
cd react-portfolio-k8s
2. Build the Docker Image
bash
Copy
Edit
docker build -t portfolio-site:latest .
3. Start Kubernetes (Minikube or Cloud)
bash
Copy
Edit
minikube start
4. Deploy to Kubernetes
bash
Copy
Edit
kubectl apply -f k8s/
5. Access the Application
If using NodePort:

bash
Copy
Edit
minikube service portfolio-service
If using Ingress:

bash
Copy
Edit
minikube addons enable ingress
kubectl apply -f k8s/ingress.yaml
