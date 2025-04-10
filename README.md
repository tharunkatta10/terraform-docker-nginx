# Terraform Docker Container on EC2

This project uses Terraform to provision a Docker container (nginx) on an EC2 instance.

## Steps

1. Run `terraform init`
2. Check plan with `terraform plan`
3. Apply changes with `terraform apply`
4. Access the app via `http://<EC2_PUBLIC_IP>:8080`
5. Destroy with `terraform destroy`

## Files
- `main.tf` - Terraform code
- `README.md` - Project instructions
