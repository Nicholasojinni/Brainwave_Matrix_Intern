Lift & Shift Application to AWS Cloud (Brainwave Matrix Intern Project)

## 📖 Project Overview
This project demonstrates how to migrate an existing on-premises/VM-based application to **AWS Cloud** using a **Lift & Shift** approach.  
The goal is to run the application in the cloud with **scalability, automation, and cost optimization**, while minimizing infrastructure management complexity.

---

## 🛑 Problem Statement
Traditional datacenter hosting has several challenges:
- ❌ Complex management of servers and teams  
- ❌ Difficulty in scaling workloads up or down  
- ❌ High upfront CAPEX and ongoing OPEX costs  
- ❌ Manual, error-prone, and time-consuming processes  

---

## ✅ Solution
Migrating workloads to AWS Cloud provides:
- ☁️ Pay-as-you-go model (no upfront CAPEX)  
- 🔄 Elastic scaling using **Auto Scaling Groups (ASG)**  
- ⚙️ Simplified infrastructure management with automation  
- 🔐 Secure access via IAM roles and policies  
- 🛡️ Improved reliability with Load Balancing & Route 53 DNS  

---

## 🔧 AWS Services Used
- **Amazon EC2** → Tomcat App server, MySQL, RabbitMQ, Memcache  
- **Elastic Load Balancer (ALB)** → HTTPS traffic distribution  
- **Auto Scaling Groups (ASG)** → Automatic scaling of Tomcat servers  
- **Amazon S3** → Artifact storage and retrieval  
- **Amazon Route 53** → DNS private zone mapping  
- **AWS Certificate Manager (ACM)** → SSL/TLS certificate for HTTPS  
- **IAM** → Secure access with roles and policies  
- **Amazon EBS** → Persistent storage for EC2 instances  

---

## 🛠️ Step-by-Step Execution

### 1. Setup Environment
- Created **key pairs** for SSH access.  
- Created **security groups** for ALB, Tomcat, and backend services.  

### 2. Provision EC2 Instances
- Launched **four EC2 instances**:
  - Tomcat server  
  - MySQL server  
  - RabbitMQ server  
  - Memcache server  
- Configured via **user data scripts**.  

### 3. Configure Route 53
- Created **private hosted zone** for internal DNS resolution.  
- Added records for backend services.  

### 4. Build & Deploy Application
- Built artifact using **Maven** locally.  
- Uploaded artifact to **Amazon S3** bucket.  
- Downloaded & deployed artifact to **Tomcat EC2 instance**.  

### 5. Setup Load Balancer
- Created **Application Load Balancer (ALB)** with HTTPS (ACM certificate).  
- Created **Target Group** for Tomcat instances.  
- Configured **health checks** on port 8080.  

### 6. Configure Auto Scaling
- Created AMI of Tomcat instance.  
- Created **Launch Template** and **Auto Scaling Group**.  
- Verified scaling in/out based on load.  

### 7. Testing
- Accessed application using public domain mapped via Route 53 & Namecheap DNS.  
- Verified high availability, scaling, and secure access.  

---

## 📂 Project Files
- **`/vprofile-project/`** → Source code & configuration  
- **`architecture.png`** → Cloud architecture diagram  
- **`/screenshots/`** → Deployment screenshots  
- **`/docs/`** → Extended documentation  


---

## 📌 Summary
By migrating this workload from a datacenter to AWS Cloud:
- Reduced operational complexity  
- Achieved automation and elasticity  
- Ensured secure, scalable, and cost-optimized deployment  

This project serves as a **practical showcase of Lift & Shift migration on AWS** and is part of my **Brainwave Matrix Internship**.

---

## 👤 Author
**Ojinni Oluwafemi Nicholas**  
- 💼 [LinkedIn](https://www.linkedin.com/in/ojinni-oluwafemi11/)  
- 🌐 [Portfolio:](https://www.stnicholastech.com/projects) 
