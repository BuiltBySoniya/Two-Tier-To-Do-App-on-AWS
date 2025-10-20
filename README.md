# 🚀 Two-Tier To-Do App on AWS

Simple Two-Tier Web Application for Task Management

## Short Description

Built a lightweight to-do list web application with a classic two-tier architecture on AWS: static front-end hosted on S3 (or served via EC2) and a backend service on EC2 communicating with an RDS database. Designed for scalability and ease of management while demonstrating foundational cloud infrastructure.

## 🛠️ AWS Services Used:

Amazon EC2,
Amazon RDS,
Amazon VPC (subnets, IGW/NAT),
Application Load Balancer (ALB),
AWS IAM,

## 🧰 Technical Tools:

HTML/CSS/JavaScript (front-end),
PHP or Node.js (backend service),
MySQL (database),
AWS CLI / SSH for deployment,

## 🧠 Skills Demonstrated:

Designing a two-tier cloud architecture,
Deploying web and database layers securely,
Configuring Load Balancer & Auto Scaling,
Securing network with subnets, NAT & security groups,

## 📋 Steps Performed

### Set Up VPC and Networking:

Created a VPC with public & private subnets across two Availability Zones.
Configured Internet Gateway for public subnet, NAT Gateway for private subnet outbound, and route tables accordingly.

### Deploy and Configure RDS Database:

Provisioned a MySQL RDS instance in the private subnet with no public access.
Created a DB subnet group spanning private subnets and attached a security group permitting only the web tier access.

### Launch Backend EC2 Instances and Install Application:

Launched web server EC2 instances in private subnets, configured with the backend code connecting to the RDS MySQL.
Installed web server (Apache/Nginx) and backend runtime, deployed to-do app code, and ensured DB connectivity.

### Create and Configure Application Load Balancer (ALB):

Set up an Internet-facing ALB in public subnets with a target group pointing to the EC2 instances in private subnets.
Configured security groups allowing inbound HTTP/HTTPS from anywhere to ALB and HTTP from ALB to web servers.

### Launch Static Front-End and Integrate with Backend:

Hosted the front-end code (HTML/JS) either on S3 static website or on the EC2 instance.
Configured the front-end to send API calls to the ALB DNS endpoint, enabled CORS and tested task-creation, update and deletion flows.

## ✅ Final Result:

Fully functional To-Do List Application on AWS with Web & Database Layers

## 💼 Business Implication:

This project demonstrates how to deploy a reliable, scalable two-tier web application on AWS with minimal complexity. By separating presentation and data layers, you improve performance and resilience, reduce single points of failure, and create a deployable architecture suitable for small business apps, internal tools, or MVPs.
