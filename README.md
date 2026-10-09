# Terraform AWS EC2 User Data Demo 🚀

This project demonstrates how to provision AWS infrastructure using Terraform and automatically install and start an Nginx web server on an EC2 instance using a User Data script.

## Project Overview

The project covers the basic infrastructure required to host a public web server on AWS. Terraform configuration is used to define networking resources and an EC2 instance, while User Data automates the initial server setup during instance launch.

## Architecture and Features

* Custom Amazon VPC
* Public subnet
* Internet Gateway
* Route table and route association
* Security group for required network traffic
* EC2 instance provisioning with Terraform
* User Data automation for Nginx installation and startup
* Terraform outputs, including the instance public IP

## Technology Stack

* **Cloud:** AWS
* **Infrastructure as Code:** Terraform
* **Web Server:** Nginx
* **Version Control:** Git and GitHub

## Repository Structure

```text
terraform-aws-ec2-userdata-demo/
├── .gitignore
├── README.md
├── main.tf
├── variables.tf
└── outputs.tf
```

## Prerequisites

* An AWS account
* Terraform CLI installed
* AWS CLI configured with appropriate credentials
* IAM permissions required to create and manage the project's resources

Never commit AWS access keys, secret keys, or other credentials to GitHub.

## Deployment Steps

### 1. Clone the repository

```bash
git clone https://github.com/akshayshendurkar55-dot/terraform-aws-ec2-userdata-demo.git
cd terraform-aws-ec2-userdata-demo
```

### 2. Initialize Terraform

```bash
terraform init
```

### 3. Format and validate the configuration

```bash
terraform fmt
terraform validate
```

### 4. Review the deployment plan

```bash
terraform plan
```

Review the resources and estimated costs before proceeding.

### 5. Deploy the infrastructure

```bash
terraform apply
```

Only confirm the operation after reviewing the plan and deciding that you are ready to incur any applicable AWS charges.

### 6. View Terraform outputs

```bash
terraform output
```

If deployment succeeds and the network and security group permit HTTP traffic, use the public IP output to test the Nginx web page in your browser.

## Security Considerations

* Restrict SSH access to your own IP address instead of allowing access from anywhere.
* Permit only the inbound traffic needed for the project.
* Use least-privilege IAM permissions.
* Do not store credentials in Terraform files or User Data scripts.

## AWS Cost Awareness and Cleanup

AWS resources may incur charges depending on their configuration, region, and current pricing. EC2, storage, and public IPv4 addresses are examples of resources that may generate costs.

When finished testing, review the resources managed by this Terraform configuration. If it is safe to remove them, run:

```bash
terraform destroy
```

Review the destruction plan before confirming. Afterwards, check the AWS Console and Billing dashboard for remaining resources and charges. Stopping an EC2 instance alone may not eliminate every cost.

## Learning Outcomes

* Understanding Infrastructure as Code with Terraform
* Learning how VPCs, subnets, gateways, route tables, and security groups work together
* Provisioning EC2 infrastructure
* Automating server setup with EC2 User Data
* Reviewing deployment plans and cleaning up AWS resources responsibly

## Author

**Laxmikant Shendurkar**

Cloud Computing and DevOps Learning Projects
