# WeCloud Chat Microservices Deployment
This project demonstrates the end-to-end process of containerizing, deploying, and managing a microservices-based chat application using Docker, Kubernetes, 
Google Cloud Platform (GCP), and Azure. 
The application is structured into separate microservices including Profile, Chat, and Login services, each with its own database and scaling configurations.  
<img src="https://github.com/JunanPan/WeCloud-Chat-Microservices/blob/intro/imgs/architecture.png" width="800px">  
## Project Overview
The WeCloud Chat application is designed to showcase cloud-native development and deployment practices. It includes the following components and features:

__Microservices Architecture (MSA)__: Each service is containerized and independently scalable.  
__Container Orchestration__: Managed Kubernetes clusters on GCP (Google Kubernetes Engine - GKE) and Azure (Azure Kubernetes Service - AKS) are used for orchestration.  
__Autoscaling__: Horizontal Pod Autoscalers (HPA) are configured to automatically scale the services based on CPU and memory usage.  
__Multi-Cloud Deployment__: The application is deployed across multiple cloud providers for high availability and resilience.  
__Helm Charts__: Helm is used to package and deploy Kubernetes applications.  
__Global Routing and Monitoring__: Azure Front Door Service is configured for global routing based on performance and availability.  
__CI/CD Automation__: GitHub Actions are utilized for continuous integration and deployment.  
<img src="https://github.com/JunanPan/WeCloud-Chat-Microservices/blob/intro/imgs/CICD.png" width="400px">  
### profile service architecture:  
<img src="https://github.com/JunanPan/WeCloud-Chat-Microservices/blob/intro/imgs/profile_microservices.png" width="400px">   

### All services together on GKE:  
<img src="https://github.com/JunanPan/WeCloud-Chat-Microservices/blob/intro/imgs/all_microservices_in_GKE.png" width="400px">  

## Getting Started
### Prerequisites:
**Docker**  
**Kubernetes**  
**Helm**  
**Google Cloud SDK**  
**Azure CLI**  
**GitHub Actions**  
### Usage
The application can be accessed through the load balancer's external IP address:  
Profile Service: `http://<load-balancer-ip>/profile?username=<username>`  
Chat Service: `http://<load-balancer-ip>/chat`  
Login Service: `http://<load-balancer-ip>/login`  
