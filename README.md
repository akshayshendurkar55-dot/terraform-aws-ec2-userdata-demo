# Terraform AWS EC2 User Data Demo

A hands-on Infrastructure as Code (IaC) project demonstrating how Terraform can provision AWS networking resources and an EC2 instance, with User Data automating Nginx installation during instance startup.

## Architecture

Terraform configuration describes these AWS resources:

* Custom VPC
* Public subnet
* Internet Gateway
* Route table and route association
* Security group
* EC2 instance
* User Data script for Nginx installation
* Terraform outputs, including the instance's public IP

## Technology Stack

* AWS EC2 and VPC
* Terraform
* Nginx
* Git and GitHub

## Repository Structure

```text
terraform-aws-ec2-userdata-demo/
├── main.tf
├── variables.tf
├── outputs.tf
├── .gitignore
└── README.md
```

## Prerequisites

* Terraform CLI
* AWS CLI
* An AWS account and appropriately configured AWS credentials
* An AWS Region where the required resources are available

Use an IAM identity with only the permissions needed for this project. Do not commit AWS access keys or other credentials to GitHub.

## Deploy

Clone the repository:

```bash
git clone https://github.com/akshayshendurkar55-dot/terraform-aws-ec2-userdata-demo.git
cd terraform-aws-ec2-userdata-demo
```

Initialize and validate Terraform:

```bash
terraform init
terraform fmt -check
terraform validate
terraform plan
```

Review the plan carefully before deciding whether to create resources.

To deploy, only when you are ready and have checked the estimated cost:

```bash
terraform apply
```

If deployment succeeds, inspect the outputs:

```bash
terraform output
```

The Nginx page can be tested using the public IP output if the instance, security group, and network configuration allow HTTP traffic.

## Security Considerations

* Restrict SSH access to your own IP address instead of exposing port 22 to everyone.
* Allow only the inbound traffic required for the demonstration.
* Avoid embedding credentials in Terraform files or User Data.
* Review the security group rules and Terraform plan before deployment.

## Cost and Cleanup

**AWS resources may incur charges.** EC2 instances, storage, public IPv4 addresses, and other resources may be billable depending on their configuration and current AWS pricing.

When you have finished testing, inspect the resources managed by this Terraform configuration. If you intend to remove them, confirm that doing so is safe and then run:

```bash
terraform destroy
```

Review the destruction plan before confirming. Also check the AWS Console and Billing dashboard for any remaining resources or charges. Stopping an instance does not necessarily eliminate every cost.

## Learning Outcomes

* Defining AWS infrastructure with Terraform
* Understanding the relationship between VPC, subnet, routing, and security groups
* Provisioning an EC2 instance
* Automating initial server configuration with User Data
* Reviewing infrastructure plans and cleaning up resources responsibly

## Author

Laxmikant Shendurkar

Cloud Computing and DevOps Learning Projects
