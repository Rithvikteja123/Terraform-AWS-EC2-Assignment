# 

## Objective
To create an EC2 instance using Terraform (Infrastructure as Code).

## Tools Used
- Terraform
- AWS (EC2)
- AWS CLI

## Steps to Run

1. Initialize Terraform

terraform init


2. Preview changes

terraform plan


3. Create EC2 instance

terraform apply


4. Destroy resources (cleanup)

terraform destroy


## Configuration Details
- Region: ap-south-1 (Mumbai)
- Instance Type: t3.micro
- OS: Amazon Linux AMI
- Tag: Name = Terraform-Student-Instance

## Output
Terraform outputs the public IP of the EC2 instance after creation.

## Notes
- AWS credentials configured using AWS CLI
- Resources destroyed after testing to avoid charges