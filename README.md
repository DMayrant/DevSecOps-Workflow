# DevSecOps-Workflow 🛠️

Automation using CI/CD pipelines and while adding security scans is best practice for DevSecOps and Platform engineering. After focusing on the tradeoffs I realized by not having automation you run the risk of having configuration drifts, increased attack surface and more cognitive overhead for engineering teams. I took one of my recent systems that I deployed to us-east-1 using terraform and added deployment and security automation using Jenkins. The infrastructure contained a VPC with a combination of edge and network security with EKS deployed in a private subnets. I used a Jenkins server to automate both terraform and kubernetes workload deployment. 

link to previous project: 
🔗 https://github.com/DMayrant/Elastic-Kubernetes-Service.git

