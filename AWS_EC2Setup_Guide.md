# AWS EC2 Web Server Setup Guide

## Step 1: Create an AWS Account (Free Tier)
- Go to the [AWS Free Tier](https://aws.amazon.com/free/) and click "Create a Free Account."
- Sign up with your details and verify your email and phone number.

## Step 2: Create an IAM User
- Log in to AWS Console and navigate to **IAM**.
- Add a new user with programmatic and console access.
- Attach policies like **AmazonEC2FullAccess** or **AWSAdminAccess**.

## Step 3: Launch Your EC2 Instance
- In the EC2 Dashboard, click **Launch Instance**.
- Select an Amazon Linux 2 AMI or Ubuntu - both are free tier.
- Choose **t2.micro** as the instance type.
- Configure the instance and create a security group allowing HTTP and SSH.

## Step 4: Connect to Your EC2 Instance
- Go to **Instances** and find your new instance.
- Connect via SSH using the following command:
  ```bash
  ssh -i /path/to/your-key.pem ec2-user@your-instance-public-ip
