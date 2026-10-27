# Dockerized Web Application Deployment on Amazon EKS

##  Project Overview

This project demonstrates the deployment of a containerized New Year countdown webpage using Docker, Kubernetes, and Amazon Elastic Kubernetes Service (EKS). The application was packaged into a Docker image, pushed to Docker Hub, and deployed on Amazon EKS using Kubernetes Deployment and Service YAML files. The application was exposed to the internet through an AWS Load Balancer.

##  Technologies Used

* **AWS EC2** – Used to access and manage the Kubernetes environment.
* **Amazon EKS** – Managed Kubernetes service for running the application.
* **Docker** – Used to build the application container image.
* **Docker Hub** – Used to store the Docker image.
* **Kubernetes** – Used to deploy and manage application Pods.
* **YAML** – Used to define Kubernetes Deployment and Service configurations.
* **Apache HTTP Server** – Used to serve the static HTML webpage.

## Architecture


 New Year Countdown Webpage  ->   Dockerfile ->  Docker Image -> Docker Hub  -> Amazon EKS Cluster  -> Kubernetes Deployment -> Application Pods -> Kubernetes LoadBalancer  -> AWS Load Balancer  -> Webpage Accessible Through Browser


##  Project Workflow

1. Created a New Year countdown webpage using HTML, CSS, and JavaScript, as applicable to the application files.
2. Created a Dockerfile using the official Apache HTTP Server image.
3. Built a Docker image containing the webpage.
4. Pushed the Docker image to Docker Hub.
5. Created an Amazon EKS cluster.
6. Wrote Kubernetes YAML files to define the Deployment and LoadBalancer Service.
7. Deployed the application using `kubectl`.
8. Verified that the application Pods were running.
9. Accessed the webpage through the external AWS Load Balancer address.

## 🐳 Dockerfile

The Dockerfile uses the official Apache HTTP Server image and copies the webpage into Apache's document directory.

```dockerfile
FROM httpd
COPY index.html /usr/local/apache2/htdocs/
```

## ☸️ Kubernetes Deployment

The Kubernetes Deployment configuration specifies the container image and manages the application's Pods.

The Kubernetes Service uses `type: LoadBalancer` to expose the application externally through an AWS load balancer.

##  Key Learnings

* Building Docker images for web applications.
* Pushing and managing container images using Docker Hub.
* Deploying applications on Amazon EKS.
* Creating Kubernetes Deployments and Services.
* Using a LoadBalancer Service to expose an application externally.
* Verifying application deployment and Pod status using `kubectl`.
