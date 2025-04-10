# Terraform Docker NGINX on EC2

This project provisions an NGINX Docker container on an AWS EC2 instance using Terraform Infrastructure as Code (IaC).

## 🛠️ Tools Used
- Terraform
- Docker
- EC2 (Ubuntu)
- GitHub

## 🚀 Features
- Uses Docker provider in Terraform
- Pulls `nginx:latest` image
- Runs container exposing port 8080
- Fully reproducible with `terraform apply`

## 📦 Files
- `main.tf` – Terraform configuration
- `.gitignore` – excludes state/log files
- `init.log`, `plan.log`, `apply.log` – Terraform output logs

## 🧪 Commands

Initialize:
```bash
terraform init | tee init.log

