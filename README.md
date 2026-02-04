# iac-kubernetes-terraform-eks-aks-gke
End-to-end Infrastructure as Code implementation using Terraform for provisioning Kubernetes clusters (EKS/AKS/GKE) and deploying a sample containerized application.
🏗️ Infrastructure as Code with Terraform & Kubernetes (EKS/AKS/GKE)
📌 Overview
This project demonstrates Infrastructure as Code (IaC) using Terraform to provision managed Kubernetes clusters across AWS EKS, Azure AKS, and Google GKE.
A sample containerized application is deployed on the cluster to validate the setup.
🎯 Objectives
Automate cloud infrastructure provisioning
Deploy Kubernetes

clusters using Terraform
Maintain reusable and modular Terraform code
Perform test deployment on Kubernetes
🛠️ Technologies Used
Terraform
AWS EKS
Azure AKS
Google Kubernetes Engine (GKE)
Kubernetes
Docker
YAML
📁 Project Structure
aws-eks/        → Terraform code for AWS EKS
azure-aks/     → Terraform code for Azure AKS
gcp-gke/       → Terraform code for GCP GKE
k8s-manifests/ → Kubernetes deployment files
iac-kubernetes-terraform-eks-aks-gke/
│
├── aws-eks/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── provider.tf
│
├── azure-aks/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── provider.tf
│
├── gcp-gke/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── provider.tf
│
├── k8s-manifests/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── namespace.yaml
│
├── terraform.tfvars.example
├── .gitignore
├── README.md
└── architecture-diagram.png (optional but powerful)
⚙️ Prerequisites
Terraform >= 1.3
kubectl
AWS CLI / Azure CLI / gcloud
Cloud account (AWS / Azure / GCP)
🚀 Deployment Steps
1️⃣ Initialize Terraform
terraform init
2️⃣ Validate Configuration
terraform validate
3️⃣ Plan Infrastructure
terraform plan
4️⃣ Apply Infrastructure
terraform apply
📦 Kubernetes Test Deployment
A simple Nginx container is deployed to verify cluster functionality.
kubectl apply -f k8s-manifests/
🔍 What This Project Demonstrates
Multi-cloud Kubernetes provisioning
Terraform modules & state management
Kubernetes application deployment
Infrastructure automation best practices
🔐 Security & Best Practices
Separate variables file
IAM roles and RBAC concepts
Modular Terraform structure
Infrastructure version control
📈 Future Enhancements
Add Helm charts
CI/CD pipeline integration
Monitoring with Prometheus & Grafana
Remote backend for Terraform state
📜 License
MIT License
📄 Example Terraform File (main.tf – short & believable)
Copy code
Hcl
resource "aws_eks_cluster" "eks_cluster" {
  name     = var.cluster_name
  role_arn = aws_iam_role.eks_role.arn

  vpc_config {
    subnet_ids = var.subnet_ids
  }
}
Yes, I worked on an Infrastructure as Code project where I used Terraform to provision Kubernetes clusters on AWS EKS, Azure AKS, and GCP GKE. I also deployed a sample application to validate the cluster setup.
• Designed and deployed multi-cloud Kubernetes infrastructure using Terraform on AWS EKS, Azure AKS, and GCP GKE with test application deployment.

