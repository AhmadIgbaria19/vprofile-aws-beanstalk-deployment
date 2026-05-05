# 🚀 VProfile DevOps Project – From Manual Infrastructure to AWS PaaS (Elastic Beanstalk)

---

## 📌 Overview

This project demonstrates a **real-world DevOps transition**:

> From manually provisioning infrastructure → to fully managed cloud deployment using AWS Elastic Beanstalk.

The application (**VProfile**) was previously deployed manually using EC2, Load Balancer, Auto Scaling, and manual configuration.

In this project, we **re-architect the deployment using AWS PaaS**, dramatically reducing complexity and improving scalability.

---

## ⚔️ Manual vs Elastic Beanstalk

| Feature | Manual Deployment | Elastic Beanstalk |
|--------|------------------|-------------------|
| EC2 Setup | Manual | Automated |
| Load Balancer | Manual | Automatic |
| Auto Scaling | Manual | Automatic |
| Deployment | Manual (SSH + Copy) | One-click Deploy |
| Monitoring | Manual | Built-in |
| Complexity | High ❌ | Low ✔ |
| DevOps Maturity | Basic | Intermediate |

---

## 🧠 Key Concept

> Elastic Beanstalk abstracts infrastructure complexity and allows DevOps engineers to focus on application deployment rather than server management.

---

## 🏗️ Architecture

[[Architecture](screenshots/architecture.png)

---

## ⚙️ Technologies Used

- AWS Elastic Beanstalk
- AWS RDS (MySQL)
- AWS ElastiCache (Memcached)
- AWS Amazon MQ (RabbitMQ)
- EC2 (Managed)
- Application Load Balancer
- Auto Scaling Group
- Maven
- Java (Spring)

---

# 🧩 Step 1 – Backend Services Setup

## 🟢 RDS

[[RDS](screenshots/rds.png)

---

## 🔵 ElastiCache

[[Cache](screenshots/cache.png)

---

## 🟣 Amazon MQ

[[RabbitMQ](screenshots/rabbit.png)

---

# ⚙️ Step 2 – Create Elastic Beanstalk Environment

This is the core step where AWS automatically provisions:

- EC2 Instances
- Load Balancer
- Auto Scaling Group
- Security Groups
- Deployment Engine

---

## 🔧 Create Application & Environment

[[Beanstalk Create Step 1](screenshots/step1.png)
[[Beanstalk Create Step 2-3](screenshots/step23.png)
[[Beanstalk Create Step 4](screenshots/step4.png)
[[Beanstalk Create Step 5](screenshots/step5.png)

---

## 🔍 Result

After creation:

✔ Load Balancer created  
✔ Auto Scaling enabled  
✔ EC2 instances running  
✔ Environment health monitoring active  

---

# 🔧 Step 3 – Application Configuration

Updated backend connections:

[[Backend Config](screenshots/backend-config.png)

---

# 🏗️ Step 4 – Build Application

```bash
mvn clean install
```

Output:

```
target/vprofile-v2.war
```

---

# 🚀 Step 5 – Deploy Application

## 📤 Upload WAR

[[Upload](screenshots/uploaddeploy.png)

---

## 🔄 Deployment Progress

[[Deploy Events](screenshots/deploy-events.png)

---

## ✅ Deployment Completed

[[Deploy Success](screenshots/deploy-success.png)

---

# 🔄 Deployment Strategy

- Rolling Deployment
- Batch size: 50%
- Zero downtime

---

# 🌐 Step 6 – Application Access

## 🔐 Login Page

[[Login](screenshots/login.png)

---

## 🎉 Dashboard

[[Dashboard](screenshots/dashboard.png)

---

# 🧪 Verification

✔ Database connected  
✔ Cache working  
✔ RabbitMQ working  
✔ Full application functionality  

---

# 📊 AWS Features Demonstrated

- Auto Scaling
- Load Balancer
- Managed Deployment
- Health Monitoring
- Service Integration

---

# 🔐 Security

- All services inside VPC
- No public backend exposure
- Secure internal communication

---

# 💡 Key Learnings

- Transition from manual to managed infrastructure
- Understanding PaaS abstraction
- Deployment strategies (Rolling)
- Service integration challenges
- Real-world debugging

---

# 🚀 Future Improvements

- Terraform (IaC)
- CI/CD Pipeline
- Dockerization
- Kubernetes (EKS)

---

# 🧠 DevOps Insight

> “A DevOps engineer's goal is not to manage servers, but to automate systems that manage themselves.”

---

# 👨‍💻 Author

Ahmad Igbaria  
DevOps Engineer (In Progress 🚀)
