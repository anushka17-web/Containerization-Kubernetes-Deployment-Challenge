# Cloud-Native Web Application Deployment Using Docker and Kubernetes

## 1. Project Overview

This project focuses on deploying a web application in a cloud environment using Docker containerization and Kubernetes orchestration.

The application is hosted on an AWS EC2 Ubuntu instance, with K3s providing lightweight Kubernetes cluster management. Nginx is used as the web server to deliver the application.

## 2. Technologies and Tools

- **AWS EC2** – Cloud computing infrastructure
- **Ubuntu** – Operating system
- **Docker** – Containerization platform
- **Kubernetes (K3s)** – Container orchestration
- **Nginx** – Web server
- **HTML and CSS** – Frontend technologies

## 3. Project Directory Structure

```text
cloud-native-web-app/
│
├── index.html
├── Dockerfile
├── deployment.yaml
├── service.yaml
└── README.md
```

### File Description

| File | Description |
|---|---|
| index.html | Main web application |
| Dockerfile | Instructions for creating the Docker image |
| deployment.yaml | Kubernetes deployment configuration |
| service.yaml | NodePort service configuration |
| README.md | Project documentation |

## 4. Docker Image Creation

Build the Docker image from the project directory using:

```bash
sudo docker build -t cnd-web-app:v1 .
```

## 5. Kubernetes Deployment

Deploy the application using the Kubernetes configuration files.

**Apply Deployment:**

```bash
sudo kubectl apply -f deployment.yaml
```

**Apply Service:**

```bash
sudo kubectl apply -f service.yaml
```

## 6. Deployment Verification

The following commands can be used to inspect the deployment:

```bash
sudo kubectl get deployments
sudo kubectl get pods
sudo kubectl get services
```

### Deployment Status

| Parameter | Status |
|---|---|
| Desired Replicas | 2 |
| Available Replicas | 2 |
| Running Application Pods | 2 |
| Service Type | NodePort |
| NodePort | 30080 |

## 7. Application Access

The application is exposed through the Kubernetes NodePort service.

**Public Application URL:**

http://3.26.171.122:30080

## 8. Key Project Outcomes

- Successfully containerized a web application using Docker.
- Used Kubernetes K3s for application deployment.
- Configured multiple application replicas.
- Exposed the application through a NodePort service.
- Utilized AWS EC2 for cloud-based hosting.
- Explored container orchestration and cloud-native deployment concepts.

## 9. Student Information

**Name:** Anushka Ghule  
**PRN / Roll Number:** 202301070127  
**Branch:** Electronics and Telecommunication (E&TC)  
**Semester:** 7th  
**Subject:** Cloud Native DevOps (MDM)
