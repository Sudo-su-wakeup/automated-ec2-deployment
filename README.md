# Automated EC2 Deployment Using AWS CloudFormation

## Project Overview

This project automates the deployment of a web server on Amazon EC2 using AWS CloudFormation.

Infrastructure is defined using YAML, while EC2 User Data automatically installs and configures Nginx when the instance launches.

## Technologies Used

- AWS CloudFormation
- Amazon EC2
- Amazon Linux 2023
- AWS VPC and Security Groups
- Nginx
- YAML
- Bash scripting

## Architecture

1. CloudFormation provisions the required AWS resources.
2. An EC2 instance launches in the selected subnet.
3. EC2 User Data installs and starts Nginx.
4. A custom HTML webpage is deployed automatically.
5. CloudFormation Outputs provide the instance ID, public IP, and website URL.

## Features

- Infrastructure as Code using CloudFormation
- Automated EC2 provisioning
- Automated Nginx installation
- Security group configuration
- Resource tagging
- CloudFormation deployment outputs

## Project Screenshots

### CloudFormation Stack

![CloudFormation Stack](screenshots/cloudformation-stack.png)

### EC2 Instance

![EC2 Instance](screenshots/ec2-instance.png)

### Deployed Website

![Deployed Website](screenshots/deployed-website.png)

## Deployment Instructions

1. Open AWS CloudFormation.
2. Upload `ec2-webserver.yaml`.
3. Provide the stack name, VPC, subnet, and instance type.
4. Create the stack.
5. Wait for the stack status to become `CREATE_COMPLETE`.
6. Open the website URL in the Outputs tab.

## Security Considerations

- HTTP access is permitted on port 80.
- SSH access is not opened to the internet by this template.
- AWS credentials must never be committed to the repository.
- This is a learning project and is not production-hardened.

## Cleanup

Delete the CloudFormation stack after testing to remove its managed resources and help avoid ongoing AWS charges.

## Learning Outcomes

This project demonstrates practical knowledge of AWS CloudFormation, EC2 provisioning, security groups, Linux initialization, Bash scripting, and automated deployment.