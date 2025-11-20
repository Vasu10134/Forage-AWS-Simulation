# Task 1: Designing a Simple, Scalable Hosting Architecture

## AWS – The Basics
AWS (Amazon Web Services) is a cloud platform that provides on-demand computing power, storage, databases, and deployment tools.  
You scale resources whenever needed and pay only for what you use.

In short:
- Need servers? AWS gives virtual machines.
- Need file storage? AWS provides cloud storage.
- Need databases, load balancers, CI/CD pipelines? Fully managed.
- Need easy app deployment? AWS automates infrastructure setup.

AWS helps you build applications that are **scalable**, **cost-efficient**, **secure**, and **highly available**.

---

## Core AWS Services

### **1. CodePipeline**
- CI/CD pipeline service.
- Builds code and deploys it to AWS (e.g., Elastic Beanstalk).
- Charged per pipeline.
- Supports blue/green zero-downtime deployments.

---

### **2. Elastic Load Balancing (ELB)**
- Distributes incoming traffic across servers (EC2, Fargate, Lambda).
- Performs health checks to avoid routing traffic to unhealthy servers.
- Pricing: running hours + data processed.
- Improves uptime and reliability.

---

### **3. RDS (Relational Database Service)**
- Managed SQL databases (MySQL, PostgreSQL, etc.).
- Billed like EC2: instance size + storage.
- Can be resized (requires restart).
- Provides backups, scaling, and maintenance.

---

### **4. Route 53**
- Domain registration and DNS management.
- Routes users to your application.
- Pricing: hosted zone cost + DNS query charges.

---

### **5. S3 (Simple Storage Service)**
- Cloud object storage for files, images, logs, backups.
- Charges: storage used + data transfer + retrieval type.
- Very durable (11 nines).
- Can host static websites.

---

## Application Execution Options

### **6. EC2**
- Full-control virtual servers.
- Pay per hour based on CPU, RAM, storage.
- Good for customizable server setups.
- Scaling needs orchestration; resizing requires restart.

---

### **7. Fargate**
- Runs containerized applications without managing servers.
- Charged by CPU/RAM per second.
- Flexible and scalable.
- Requires defining tasks and services.

---

### **8. Lambda**
- Serverless functions triggered by events (HTTP, S3, etc.).
- Pay only for execution time + memory + number of requests.
- Highly scalable.
- Not ideal for serving static content or long-running processes.

---

### **9. Lightsail**
- Simple virtual machines with predictable monthly pricing.
- Good for small apps, blogs, prototypes.
- Limited flexibility; scaling requires cloning.

---

### **10. Elastic Beanstalk**
- Automates deployment using EC2 + Load Balancer + RDS + autoscaling.
- Supports Node, Python, Java, Go, and more.
- Easy CLI-based deployments.
- Blue/green and rolling deployment support.
- Pricing = cost of underlying EC2 + RDS + ELB resources.

---

## Availability Zones (AZs)
- AWS regions are divided into multiple AZs.
- Deploying services across AZs increases redundancy.
- Cost multiplies because resources are duplicated.

---

## Why Elastic Beanstalk for This Architecture
- Automatically manages EC2, Load Balancer, autoscaling, and deployments.
- Reduces manual infrastructure management.
- Supports enterprise deployment strategies like rolling and blue/green.
- Still gives access to underlying resources when needed.

---

## Pricing Note
- Pricing varies by region.
- Billing style remains consistent:  
  - EC2/RDS: hourly rate  
  - S3: storage + retrieval  
  - Lambda: execution time  
  - ELB: running hours + traffic  
- Use AWS Pricing Calculator for estimates.

