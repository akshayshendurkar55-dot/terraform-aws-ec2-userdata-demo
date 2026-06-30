# Terraform AWS EC2 User Data Demo 🚀

This project demonstrates how to launch an AWS EC2 instance using Terraform and automatically deploy an Nginx web server using User Data.

## Project Overview

In this project, I created an AWS EC2 instance inside a custom VPC using Terraform. I configured a public subnet, Internet Gateway, Route Table, Security Group, and User Data script to automatically install and start Nginx during instance launch.

## Technologies Used

- Terraform
- AWS EC2
- AWS VPC
- AWS Security Group
- Nginx
- Git
- GitHub

## Features

- Custom VPC creation
- Public Subnet creation
- Internet Gateway and Route Table setup
- Security Group allowing SSH and HTTP
- EC2 instance provisioning
- User Data automation
- Automatic Nginx installation
- Public IP output

## Terraform Commands Used

```bash
terraform init
terraform validate
terraform plan
terraform apply
terraform output
terraform destroy
Output
Successfully launched an EC2 instance using Terraform and hosted a live Nginx webpage using User Data automation.
Learning Outcome
I learned how to automate EC2 server setup using Terraform User Data. I also understood how VPC, Subnet, Internet Gateway, Route Table, Security Group, and EC2 work together to host a public web server.
Author
Laxmikant Shendurkar