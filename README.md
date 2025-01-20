# secure-docker-image-build-calico
secure Docker image build project usign Calico and Terraform

# Kubernetes Network Policies with Calico and Terraform

## Overview

This project demonstrates how to implement Kubernetes network policies using Calico and Terraform. It includes:
- A Kubernetes cluster provisioned via Terraform
- Calico as the CNI plugin
- Network policies for:
  - Denying all traffic by default
  - Allowing frontend-to-backend communication
  - Isolating namespaces

## Prerequisites
- Terraform
- kubectl
- AWS CLI (for EKS)
- An AWS account

## Project Structure


![image](https://github.com/user-attachments/assets/266f4a56-02d7-4a52-9a93-ed318be9d8fd)




## Steps

1. **Provision the Kubernetes Cluster**
   ```bash
   terraform init
   terraform apply

2. **Set Up Calico**
   ```bash
   ./scripts/setup-calico.sh

3. **Deploy Applications**
   ```bash
   kubectl apply -f k8s/deployments/frontend.yaml
   kubectl apply -f k8s/deployments/backend.yaml

4. **Apply Network Policies**
   ```bash
   kubectl apply -f k8s/network-policies/


**Features**

Deny all traffic by default.
Enable frontend-to-backend communication.
Isolate namespaces for enhanced security.

Cleanup

**To destroy resources:**
```bash
terraform destroy
