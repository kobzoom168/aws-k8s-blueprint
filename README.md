# AWS Kubernetes Blueprint

## 📌 Overview
AWS Kubernetes Blueprint provides a ready-to-use Terraform configuration for deploying an Amazon EKS cluster with best practices.

## 🚀 Features
- **Automated Amazon EKS Cluster Deployment** using Terraform
- **Managed Node Groups** for scalable workloads
- **IAM Roles & Policies** preconfigured for Kubernetes
- **Helm support** for deploying applications

## 📂 Folder Structure
```
aws-k8s-blueprint/
├── terraform/   # Terraform scripts for EKS
├── helm/        # Helm charts for Kubernetes apps
├── scripts/     # Helper scripts for automation
├── README.md    # Documentation
```

## 🛠 Prerequisites
- AWS CLI configured (`aws configure`)
- Terraform installed (`terraform -v`)
- kubectl installed (`kubectl version`)
- Helm installed (`helm version`)

## ⚡ Deployment Steps

### **Step 1: Clone the Repository**
```sh
git clone https://github.com/your-org/aws-k8s-blueprint.git
cd aws-k8s-blueprint
```

### **Step 2: Deploy EKS with Terraform**
```sh
cd terraform
terraform init
terraform apply -auto-approve
```

### **Step 3: Configure kubectl for EKS**
```sh
aws eks update-kubeconfig --name my-eks-cluster --region us-east-1
kubectl get nodes
```

### **Step 4: Deploy Applications Using Helm**
```sh
cd ../helm
helm install my-app ./my-app-chart/
```

## 🎯 Usage
- Once EKS is running, you can deploy applications using `kubectl` or Helm
- Use `kubectl port-forward` for local access to services

## 🔄 Cleanup
To delete the EKS cluster:
```sh
cd terraform
terraform destroy -auto-approve
```

## 📖 Documentation
For more details, refer to [AWS EKS Docs](https://docs.aws.amazon.com/eks/latest/userguide/) and [Terraform EKS Docs](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/eks_cluster).

## 📌 License
This project is licensed under the MIT License.

