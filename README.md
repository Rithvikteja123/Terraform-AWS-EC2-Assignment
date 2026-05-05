# Terraform AWS EC2 Assignment

## Objective

The objective of this assignment is to understand Infrastructure as Code (IaC) using Terraform by creating and managing an AWS EC2 instance.

---

## 🛠️ Tools & Technologies

* Terraform
* AWS (EC2)
* AWS CLI
* Git & GitHub

---

## Project Structure

```
terraform-aws-assignment/
├── main.tf
├── README.md
├── .gitignore
├── .terraform.lock.hcl
```

---

##  Configuration Details

* **Provider**: AWS
* **Region**: ap-south-1 (Mumbai)
* **Instance Type**: t3.micro
* **AMI**: Amazon Linux
* **Tag Name**: Terraform-Student-Instance

---

## Terraform Code Overview

### Provider Configuration

Defines AWS as the cloud provider and specifies the region.

```hcl
provider "aws" {
  region = "ap-south-1"
}
```

---

### EC2 Resource

Creates an EC2 instance with required configuration.

```hcl
resource "aws_instance" "my_instance" {
  ami           = "ami-0f58b397bc5c1f2e8"
  instance_type = "t3.micro"

  tags = {
    Name = "Terraform-Student-Instance"
  }
}
```

---

### Output

Displays the public IP address of the created EC2 instance.

```hcl
output "instance_public_ip" {
  value = aws_instance.my_instance.public_ip
}
```

---

## Steps to Execute

### 1. Initialize Terraform

```
terraform init
```

### 2. Preview Execution Plan

```
terraform plan
```

### 3. Create Infrastructure

```
terraform apply
```

Type `yes` to confirm.

### 4. Destroy Infrastructure (Cleanup)


##  Output

After successful execution, Terraform provides:

* Public IP of the EC2 instance



##  Repository

GitHub Repository:
https://github.com/Rithvikteja123/Terraform-AWS-EC2-Assignment
