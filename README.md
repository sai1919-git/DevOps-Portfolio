# 🚀 DevOps Portfolio – Sai Gulipalli

## About Me
Aspiring DevOps fresher with hands-on experience in AWS, Linux, Git, Docker, Jenkins, Kubernetes,maven,terraform and monitoring tools.  
I focus on building, deploying, automating, and monitoring applications in cloud environments.
## 🧩 Projects

### 🔹 Project 1: Manual Deployment on AWS EC2
**Tools: AWS EC2, Ubuntu Linux, GitHub, Nginx  
**Description:**
Deployed a static HTML application manually on an Ubuntu EC2 instance using GitHub and Linux.  
🔗 Repository: https://github.com/sai1919-git/projects/tree/main/project-1

## Tools
- AWS (EC2, IAM)
- Linux (Ubuntu)
- Git & GitHub
- Nginx

## 🎯 Goal
To understand how web applications are hosted in real environments by setting up an Nginx web server on AWS EC2 and manually deploying application code using Linux and Git.


### 🔹 Project 2: Dockerized Python Application

**Description:** 
Built a Python Flask web application and containerized it using Docker by creating a Dockerfile.
The Docker image was built and deployed on an AWS EC2 Ubuntu instance with proper port mapping.
This project helped me understand Docker images vs containers and real-world containerized deployment.
🔗 Repository: https://github.com/sai1919-git/projects/tree/main/project-2

## Tools Used
- Python (Flask)
- Docker
- Git & GitHub
- AWS EC2 (Ubuntu)

## What I Did
- Created a simple Python Flask web application
- Wrote a Dockerfile to containerize the app
- Built Docker image locally and on EC2
- Ran the container using port mapping
- Accessed the application via EC2 public IP

## Docker Commands Used
```bash
docker build -t python-flask-app .
docker run -d -p 80:5000 python-flask-app
'''

## 🎯 Goal
The goal of this project is to understand how applications can be packaged and deployed consistently across environments using Docker.
By containerizing a Python web application, I aimed to eliminate environment dependency issues and learn how modern applications are deployed using containers on cloud servers.


###🔹** Project 3: CI Pipeline with Jenkins (Build + Test)

**Description:**
Implemented a Continuous Integration (CI) pipeline using Jenkins to automate the build and deployment of a Dockerized Python Flask application.
The pipeline pulls code from GitHub, builds a Docker image, removes any existing container, and deploys the latest version automatically on an AWS EC2 instance.
This project helped me understand real-world CI workflows, Jenkins declarative pipelines, and Docker automation on cloud infrastructure.

🔗 Repository:
https://github.com/sai1919-git/projects/tree/main/project-3

## Tools Used
Jenkins
Docker
Python (Flask)
Git & GitHub
AWS EC2 (Ubuntu Linux)

## What I Did

Created a Python Flask web application
Containerized the application using Docker
Installed and configured Jenkins on AWS EC2
Wrote a Declarative Jenkinsfile for CI automation
Configured GitHub webhook to trigger Jenkins builds on code push
Automated Docker image build and container deployment
Managed container cleanup to avoid port conflicts
Deployed and accessed the application via EC2 public IP

⚙️ Jenkins Pipeline Steps
Jenkins pulls the latest code from GitHub
Builds a Docker image for the Flask application
Removes any existing running container
Runs a new container in detached mode with port mapping

## Docker Commands Used
'''
docker build -t project3-app .
docker rm -f $(docker ps -aq --filter ancestor=project3-app)
docker run -d -p 5000:5000 project3-app
'''

🎯 Goal
The goal of this project is to understand how CI pipelines automate application builds and deployments using Jenkins and Docker.
By integrating GitHub, Jenkins, Docker, and AWS EC2, I learned how real-world DevOps teams continuously build and deploy applications reliably and efficiently.









