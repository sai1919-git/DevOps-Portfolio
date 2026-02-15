# 🚀 DevOps Portfolio – Sai Gulipalli

## 👤 About Me
Aspiring DevOps fresher with hands-on experience in AWS, Linux, Git, Docker, Jenkins, Kubernetes, Maven, Terraform, and monitoring tools.  
I focus on building, deploying, automating, and monitoring applications in cloud environments.

---

## 🧩 Projects

---

## 🔹 Project 1: Manual Deployment on AWS EC2

### 📌 Description
Deployed a static HTML application manually on an Ubuntu EC2 instance using GitHub and Linux.  
Configured **Nginx** as a web server and hosted the application using the EC2 public IP.

🔗 **Repository:**  
https://github.com/sai1919-git/projects/tree/main/project-1

### 🛠️ Tools Used
- AWS EC2
- Ubuntu Linux
- Git & GitHub
- Nginx

### ✅ What I Did
- Launched an Ubuntu EC2 instance
- Installed and configured Nginx web server
- Cloned application code from GitHub
- Deployed static website manually
- Verified application using EC2 public IP

### 🎯 Goal
To understand how web applications are hosted in real environments by manually deploying application code on AWS EC2 using Linux and Nginx.

---

## 🔹 Project 2: Dockerized Python Flask Application

### 📌 Description
Built a Python Flask web application and containerized it using Docker by creating a Dockerfile.  
The Docker image was built and deployed on an AWS EC2 Ubuntu instance with proper port mapping.  
This project helped me understand **Docker images vs containers** and real-world containerized deployments.

🔗 **Repository:**  
https://github.com/sai1919-git/projects/tree/main/project-2

### 🛠️ Tools Used
- Python (Flask)
- Docker
- Git & GitHub
- AWS EC2 (Ubuntu)

### ✅ What I Did
- Created a Python Flask web application
- Wrote a Dockerfile to containerize the application
- Built Docker image locally and on EC2
- Ran the container using port mapping
- Accessed the application via EC2 public IP

### 🐳 Docker Commands Used
```bash
docker build -t python-flask-app .
docker run -d -p 80:5000 python-flask-app
```
### 🎯 Goal
To understand how applications can be packaged and deployed consistently across environments using Docker and containers.

---

## 🔹 Project 3: CI Pipeline with Jenkins (Dockerized Flask App)

### 📌 Description
Implemented a **Continuous Integration (CI) pipeline** using Jenkins to automate the build and deployment of a Dockerized Python Flask application.  
The Jenkins pipeline automatically pulls source code from GitHub, builds a Docker image, removes any existing container, and deploys the latest version on an AWS EC2 instance.

This project provided hands-on experience with **real-world CI workflows**, **Jenkins Declarative Pipelines**, and **Docker automation** on cloud infrastructure.

🔗 **Repository:**  
https://github.com/sai1919-git/projects/tree/main/project-3

### 🛠️ Tools Used
- Jenkins  
- Docker  
- Python (Flask)  
- Git & GitHub  
- AWS EC2 (Ubuntu Linux)


### ✅ What I Did
- Built a CI pipeline using Jenkins for a Dockerized Flask application
- Created and maintained a Dockerfile for the Flask app
- Installed and configured Jenkins on an AWS EC2 Ubuntu instance
- Connected Jenkins with a GitHub repository for source code management
- Wrote a Declarative Jenkinsfile to automate the CI workflow
- Automated Docker image build on every Jenkins pipeline run
- Removed existing Docker containers to avoid port conflicts
- Deployed the latest Docker container automatically after build
- Verified application deployment using the EC2 public IP


### ⚙️ Jenkins Pipeline Flow
1. Jenkins pulls the latest code from GitHub  
2. Docker image is built from the Dockerfile  
3. Existing container (if any) is removed  
4. New container is started in detached mode with port mapping  

### 🐳 Docker Commands Used
```bash
docker build -t project3-app .
docker rm -f $(docker ps -aq --filter ancestor=project3-app)
docker run -d -p 5000:5000 project3-app
```
### 🎯 Goal
To understand how CI pipelines automate application builds and deployments using Jenkins and Docker. By integrating GitHub, Jenkins, Docker, and AWS EC2, I learned how real DevOps teams continuously build and deploy applications efficiently.

---
## 🔹 Project 4: CI Pipeline with Jenkins (Dockerized Flask App pushed to AWS ECR)

### 📌 Description
Implemented a Continuous Integration (CI) pipeline using Jenkins to automate the build and push of a Dockerized Python Flask application to AWS Elastic Container Registry (ECR).
The Jenkins pipeline automatically pulls source code from GitHub, builds a Docker image, logs in securely to AWS ECR, tags the image, and pushes it to the ECR repository.
This project provided hands-on experience with real-world CI workflows, Jenkins Declarative Pipelines, Docker automation, and cloud container registries.

### 🔗 Repository:
https://github.com/sai1919-git/projects/tree/main/project-4

### 🛠️ Tools Used
Jenkins
Docker
Python (Flask)
Git & GitHub
AWS EC2 (Ubuntu Linux)
AWS ECR

### ✅ What I Did
- Created a Python Flask web application
- Containerized the application using Docker
- Installed and configured Jenkins on AWS EC2
- Added AWS credentials securely in Jenkins
- Wrote a Declarative Jenkinsfile for CI
- Integrated GitHub repository with Jenkins
- Automated Docker image build, tag, and push to AWS ECR
- Verified the pushed images in AWS ECR

### ⚙️ Jenkins Pipeline Flow
1. Jenkins pulls the latest code from GitHub
2. Docker image is built from the Dockerfile
3. Jenkins logs in securely to AWS ECR using credentials
4. Docker image is tagged with the build number
5. Docker image is pushed to the AWS ECR repository

### 🐳 Docker Commands Used

```bash
docker build -t project4image:$BUILD_NUMBER .
docker tag project4image:$BUILD_NUMBER 64194****.dkr.ecr.ap-south-1.amazonaws.com/project-4:$BUILD_NUMBER
docker push 64194****.dkr.ecr.ap-south-1.amazonaws.com/project-4:$BUILD_NUMBER
```

### 🎯 Goal
To understand how CI pipelines integrate Jenkins, Docker, and AWS ECR to automate image builds and secure cloud registry management.
By implementing this project, I learned how real DevOps teams continuously build, tag, and push containerized applications efficiently.

---


## 🔹 Project 5: cloud native application deployment using AWS kubernetes (AWS EKS) 

### 📌 Description
Deployed a Python Flask application on AWS EKS using Docker containers.
The project involved building a Docker image, pushing it to AWS ECR, deploying it on an EKS cluster, and exposing it using a LoadBalancer.
This project provided hands-on experience with Kubernetes deployments, EKS architecture, worker nodes, and cloud-based load balancing.

### 🔗 Repository:
https://github.com/sai1919-git/projects/tree/main/project-5

### 🛠️ Tools Used
AWS EKS
AWS EC2 (Ubuntu Linux)
AWS ECR
Docker
kubectl
eksctl
Python 

### ✅ What I Did
- Created a Python application
- Containerized the application using Docker
- Created an EKS cluster using eksctl
- Deployed the Docker image on EKS pods
- Exposed the application via a LoadBalancer service
- Verified the application was running using the LoadBalancer DNS
- Cleaned up AWS resources (EKS cluster, EC2, ECR, LoadBalancer)

### ⚙️ Deployment Flow
- Build Docker image from the Flask application
- Tag Docker image and push to AWS ECR
- Create an EKS cluster using eksctl
- Deploy the application using Kubernetes Deployment
- Expose the application using a LoadBalancer service
- Access the application via the external LoadBalancer DNS
  
### 🐳 Docker / ECR Commands
```bash
docker build -t eks-app .
aws ecr get-login-password --region <REGION> | docker login --username AWS --password-stdin <AWS_ACCOUNT_ID>.dkr.ecr.<REGION>.amazonaws.com
docker tag eks-app:latest <ECR_URI>:latest
docker push <ECR_URI>:latest
```
### 🖥️ kubectl & eksctl Commands Used
```bash
# Create EKS cluster
eksctl create cluster \
  --name project-5 \
  --region ap-south-1 \
  --nodegroup-name project-5-nodes \
  --node-type t3.medium \
  --nodes 2 \
  --nodes-min 1 \
  --nodes-max 3 \
  --managed

kubectl get nodes
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get svc eks-app-service -w
eksctl delete cluster --name project-5 --region ap-south-1
```

### 🎯 Goal
To learn containerized application deployment on AWS EKS, including Docker image management with AWS ECR, Kubernetes deployments, and exposing services via LoadBalancer.
This project demonstrates practical DevOps skills in deploying applications to a production-ready cloud environment.

---


