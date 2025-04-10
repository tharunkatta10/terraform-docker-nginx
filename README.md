# 🚀 Terraform Docker NGINX (on AWS EC2)

This project provisions an **NGINX web server** running inside a **Docker container** using **Terraform**, fully deployed on an **AWS EC2 instance**.

---

## 🛠️ Tech Stack

- Terraform
- Docker
- NGINX
- AWS EC2 (Ubuntu)

---

## 📦 What It Does

- Uses Terraform's Docker provider to:
  - Pull the official NGINX image
  - Launch a Docker container on port 8080
- Automatically configures and runs on an EC2 instance

---

## 📂 Project Structure

```
terraform-docker-nginx/
├── main.tf            # Terraform configuration file
├── README.md          # Project documentation
├── init.log           # Output log for terraform init
├── plan.log           # Output log for terraform plan
├── apply.log          # Output log for terraform apply
├── destroy.log        # Output log for terraform destroy
└── .gitignore         # Ignored files/folders
```

---

## 🚀 How to Deploy

> All commands are to be run on your EC2 instance.

### 1. Initialize Terraform

```bash
terraform init | tee init.log
```

### 2. Preview the plan

```bash
terraform plan | tee plan.log
```

### 3. Apply the plan (Deploy container)

```bash
terraform apply -auto-approve | tee apply.log
```

### 4. Test the NGINX server

```bash
curl localhost:8080
```

Or from your browser:

```
http://<your-ec2-public-ip>:8080
```

> Make sure port 8080 is open in your EC2 security group.

---

## 🧹 Cleanup

To destroy the container and image:

```bash
terraform destroy -auto-approve | tee destroy.log
```

---

## ⚠️ Notes

- Docker must be installed and running on the EC2 instance.
- This project is for learning/demo purposes. Don’t expose EC2 to 0.0.0.0 in production.
## 👨‍💻 Author

**Tharun Katta**  
[GitHub Repo](https://github.com/tharunkatta10/terraform-docker-nginx)

---


