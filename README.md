# DevSecOps-Workflow 🛠️

Automation using CI/CD pipelines and while adding security scans is best practice for DevSecOps and Platform engineering. After focusing on the tradeoffs I realized by not having automation you run the risk of having configuration drifts, increased attack surface and more cognitive overhead for engineering teams. I designed a system and deployed it to us-east-1 using terraform and added deployment and security automation using Jenkins. The infrastructure contained a VPC with a combination of edge and network security with EKS deployed in a private subnets. I used a Jenkins server to automate both terraform and kubernetes workload deployment. 

link to previous project: 
🔗 https://github.com/DMayrant/Elastic-Kubernetes-Service.git

![image alt](https://github.com/DMayrant/DevSecOps-Workflow/blob/main/CI:CD%20Pipeline.jpeg?raw=true)


![image alt](https://github.com/DMayrant/DevSecOps-Workflow/blob/main/Screenshot%202569-03-25%20at%2016.27.28.png?raw=true)


# Jenkins CI/CD Pipeline 🔐

Pipeline Security 
- Trivy (container image scan)
- Tfsec (terraform configuration file scan)
- Checkov (Kubernetes YAML, JSON, and terraform config scan)
- OWASP ZAP ⚡️ (Endpoint exposure detection)
- Kubescape (Cluster hardening, NSA and MITRE compliance)


# Kubernetes ☸️

Workloads 
- ClusterIP service
- Nginx Deployment 
- Test pod for internal service discovery 
- Custom Service Account
- Namespaces 
- ResourceQuotas

# Terraform Iac Infrastructure 🏗️

Networking 🛜

- VPC ☁️ US-east-1
- Subnets (Private/Public)
- Endpoints to SSM
- ALB  

Infrastructure/Edge Security 🔐

- WAF (DDOS protection)
- Guardduty (threat detection)
- ACM (SSL/TLS certificates)

Storage 

- S3 backend with DynamoDB lock
- Object storage for ALB/SSM logs
- Aurora Database 

Observability 
- CloudWatch 
- CloudTrail 

