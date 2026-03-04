# Brain Tasks App DevOps Deployment

This project demonstrates a complete CI/CD pipeline for deploying the Brain Tasks application using AWS services.

## GitHub Repository
https://github.com/harshini-m-devops/brain-tasks-app-devops

## Technologies Used

- Docker
- AWS ECR
- AWS EKS
- Kubernetes
- AWS CodeBuild
- AWS CodePipeline
- GitHub
- CloudWatch Logs

## Project Architecture

GitHub  
↓  
CodePipeline  
↓  
CodeBuild  
↓  
Docker Build  
↓  
Push Image to ECR  
↓  
Deploy to EKS using kubectl  
↓  
Kubernetes Service (LoadBalancer)  
↓  
Application accessible via public URL  

## Steps Implemented

### 1. Application Setup
Cloned the application repository and used the production build files.

### 2. Dockerization
Created a Dockerfile to containerize the application using Nginx.

### 3. Container Registry
Created an AWS ECR repository to store Docker images.

### 4. Kubernetes Deployment
Created `deployment.yaml` and `service.yaml` to deploy the application to AWS EKS.

### 5. CI/CD Pipeline
Configured AWS CodePipeline with the following stages:

Source → GitHub  
Build → CodeBuild  
Deploy → EKS  

### 6. Monitoring
CloudWatch Logs were used to monitor build and deployment logs.

---

## Kubernetes LoadBalancer

Application URL:  
http://a328467226dd84127a21f06316c3801f-627419157.us-east-1.elb.amazonaws.com

LoadBalancer ARN:  
arn:aws:elasticloadbalancing:us-east-1:084396578047:loadbalancer/a328467226dd84127a21f06316c3801f

---

## Repository Structure

