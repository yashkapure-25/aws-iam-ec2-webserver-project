# AWS IAM & EC2 Web Server Deployment

## Project Overview

This project demonstrates how to configure AWS Identity and Access Management (IAM), launch an Amazon EC2 instance, secure network access using Security Groups, and deploy a static HTML website using Apache Web Server.

## Objectives

- Understand IAM users, groups, roles, and policies.
- Implement the principle of least privilege.
- Launch and configure an Amazon EC2 instance.
- Configure Security Groups for SSH and HTTP.
- Install Apache Web Server.
- Deploy a publicly accessible HTML website.

## Technologies Used

- Amazon Web Services (AWS)
- AWS IAM
- Amazon EC2
- Amazon Linux 2023
- Apache HTTP Server
- HTML and CSS
- GitHub

## Implementation Steps

### 1. AWS IAM Configuration
Created an IAM user and user group and attached the AmazonEC2ReadOnlyAccess policy to demonstrate least-privilege access.

### 2. EC2 Instance Deployment
Launched an Amazon EC2 instance running Amazon Linux 2023.

### 3. Security Group Configuration
Configured inbound security rules:
- SSH (Port 22): Restricted administrative access
- HTTP (Port 80): Public website access

### 4. Apache Installation
Installed and enabled Apache using:

```bash
sudo dnf update -y
sudo dnf install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### 5. Website Deployment
Created an `index.html` file and deployed it to `/var/www/html/`.

### 6. Deployment Verification
Verified that the website was accessible using the EC2 instance's public IPv4 address.

## Live Website

http://32.200.159.96

Replace this placeholder with your actual live website URL.

## Project Screenshots

Screenshots documenting IAM configuration, EC2 deployment, Security Group rules, Apache installation, and the live website are available in the `screenshots` folder.

## Security Practices

- Applied least-privilege IAM permissions.
- Restricted SSH access.
- Enabled only the required inbound ports.
- Kept private keys and credentials out of the public repository.

## Conclusion

Successfully deployed a static HTML website on AWS EC2 while gaining hands-on experience with IAM, Linux server administration, Apache, and AWS networking.
