🚀 Production-Ready Highly Available Web Architecture on AWS
Overview

This project demonstrates the design and implementation of a highly available, scalable, and secure web architecture on AWS.

The infrastructure is built using a custom VPC with public and private subnets across multiple Availability Zones, ensuring high availability and fault tolerance. Web servers are deployed in private subnets and receive traffic through an Application Load Balancer.

🏗️ Architecture
Internet
   │
Application Load Balancer
   │
Target Group
   │
Auto Scaling Group
   │
Private EC2 Instances
   │
NAT Gateway
   │
Internet Gateway
⚙️ Services Used
AWS VPC (Virtual Private Cloud)
EC2 (Elastic Compute Cloud)
Auto Scaling Group
Application Load Balancer
NAT Gateway
Internet Gateway
Security Groups
Bastion Host
🔑 Key Features
Multi-AZ deployment for high availability
Private subnet architecture for enhanced security
Load balancing across multiple EC2 instances
Auto Scaling for dynamic traffic handling
Secure access to private instances via Bastion Host
Controlled internet access using NAT Gateway
🛠️ Implementation Steps
1️⃣ VPC Setup
Created VPC using "VPC and More" option
Configured:
2 Public Subnets
2 Private Subnets
Internet Gateway
NAT Gateway (in each AZ)
2️⃣ Target Group Creation
Created Target Group with:
Protocol: HTTP
Port: 80
Registered EC2 instances
3️⃣ Auto Scaling Group
Created Launch Template
Configured Auto Scaling Group:
Desired Capacity: 2
Multi-AZ deployment
Attached Target Group
4️⃣ Bastion Host Setup
Deployed Bastion Host in Public Subnet
Enabled SSH access to private EC2 instances
5️⃣ Web Server Deployment
Installed Apache on EC2 instances
Deployed webpage in:
/var/www/html/index.html
6️⃣ Load Balancer Configuration
Created Application Load Balancer
Listener: HTTP (Port 80)
Forwarded traffic to Target Group
📸 Screenshots

Screenshots are available in the screenshots/ directory:

VPC Configuration
Target Group Setup
Auto Scaling Group
Bastion Host Connection
Load Balancer Configuration
Web Application Output
✅ Result
Successfully deployed a highly available web application
Load Balancer distributes traffic across EC2 instances
Application remains accessible even if one instance fails
📚 Key Learnings
Designing secure AWS network architecture
Working with private and public subnets
Implementing Auto Scaling and Load Balancing
Managing access using Bastion Host
Building production-style cloud infrastructure
🔮 Future Improvements
Add HTTPS using SSL/TLS (ACM)
Use Route 53 for custom domain
Automate deployment using Terraform
Add monitoring using CloudWatch
🤝 Connect With Me
LinkedIn: https://www.linkedin.com/in/devops-samarjeet/
