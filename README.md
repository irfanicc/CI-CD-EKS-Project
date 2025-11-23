# 🚀 End-to-End CI/CD Pipeline for Node.js App Deployment on Amazon EKS (GitHub Actions)

![EKS Banner](https://imgur.com/h87KAuY.png)

A fully automated **CI/CD pipeline** built using **GitHub Actions, Docker, Kubernetes, and AWS EKS** — designed to deploy a production-ready Node.js application with DevOps best practices.

---

![CI/CD Pipeline](https://imgur.com/Ctznv2m.png)

## 📌 Table of Contents  

- [📂 Repository Structure](#-repository-structure)
- [🔧 Prerequisites](#-prerequisites)
- [⚙️ CI/CD Workflow](#️-cicd-workflow)
  - [🔨 Build Job](#-build-job)
  - [🚀 Deployment Job](#-deployment-job)
- [🏗️ Infrastructure Details](#️-infrastructure-details)
- [📦 Deployment Strategy](#-application-deployment-strategy)
- [🔄 GitOps Principles](#-gitops-principles)
- [🔒 Security Best Practices](#-security-best-practices)
- [📢 Notifications & Alerts](#-notifications--alerts)
- [📊 Monitoring & Logging](#-monitoring--logging)
- [📜 Contributing](#-contributing)
- [🛠️ Author & Community](#️-author--community)
- [📧 Connect With Me](#-lets-connect)
- [⭐ Support](#-hit-the-star)

---

## 📂 Repository Structure  

Designed for **modularity, scalability**, and **production readiness**:

```tree
📂 root  
├── 📂 .github/workflows/        # CI/CD workflows
│   ├── ci.yml                   # Continuous Integration pipeline
│   └── cd.yml                   # Continuous Deployment pipeline

├── 📂 app                       # Application source code
│   ├── app.py                   # Python Flask implementation  
│   ├── calculator.js            # Business logic  
│   ├── calculator.test.js       # Unit tests  
│   ├── Dockerfile               # Optimized Node.js Dockerfile  
│   ├── Dockerfile-python        # Flask Dockerfile  
│   ├── index.js                 # Main entry point  
│   ├── package.json             # Dependencies  
│   └── requirements.txt         # Python requirements  

├── 📂 kustomize                 # Kustomize configuration
│   ├── 📂 base                  # Base Kubernetes config  
│   ├── 📂 overlays              # Env-specific configs (dev/prod/staging)

├── 📂 terraform                 # AWS Infrastructure provisioning
│   ├── main.tf
│   ├── ingress-nginx.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── terraform.tf

├── .eslintrc.js                 # ESLint config
├── docker-compose.yml           # Local development setup  
├── nginx.conf                   # Reverse proxy config  
├── .gitignore                   # Git ignore file  
├── README.md                    # Project documentation  
└── VERSION                      # Semantic versioning  
🚀 Recent Improvements
🔧 Application Enhancements
Health checks & graceful shutdown

REST API endpoint at /api/calculate

CORS enabled

Enhanced UI & performance

🐳 Docker & Security Enhancements
Multi-stage Docker build

Non-root user execution

Health checks + signal handling

☸️ Kubernetes Improvements
Probes (Liveness & Readiness)

Resource limits & security context

Zero-downtime rolling updates

🔄 CI/CD Pipeline (GitHub Actions)
Trivy security scan

ESLint + unit tests

Node 18 & 20 test matrix

Automatic Docker image push

🔧 Prerequisites
Tool	Required
Node.js	>=18.x
Docker	Yes
Terraform	>=1.0
AWS CLI & eksctl	Yes
Kustomize	Yes
kubectl	Latest
GitHub Actions	Configured
IAM Permissions	Required

🏃 Quick Start (Local Development)
▶ Option 1: Docker Compose (Recommended)
bash
Copy code
git clone https://github.com/NotHarshhaa/CI-CD_EKS-GitHub_Actions.git
cd CI-CD_EKS-GitHub_Actions
docker-compose up --build
Access:

bash
Copy code
http://localhost:80         → Web UI  
http://localhost:80/health  → Health API  
POST /api/calculate         → REST API  
▶ Option 2: Local Node.js Run
bash
Copy code
cd app
npm install
npm run dev
npm test
npm run lint
⚙️ CI/CD Workflow (GitHub Actions)
🔨 Build Stage
✔ Install dependencies
✔ Run unit tests
✔ Lint code
✔ Semantic version update
✔ Build & push Docker image → AWS ECR

🚀 Deployment Stage
✔ Terraform infra provisioning
✔ Update kubeconfig
✔ Install NGINX Ingress using Helm
✔ Apply Kustomize overlays
✔ Deploy to AWS EKS Cluster

🏗 Infrastructure Details
Environment	Instance Type	Replicas
Dev	t3.small	1
Staging	t3.medium	3
Prod	t3.large	3

✔ DNS via Cloudflare
✔ Subdomains →

Copy code
dev.example.com  
staging.example.com  
prod.example.com  
📦 Application Deployment Strategy
Strategy	Usage
Rolling Update	Default
Blue-Green	Production
Canary	Test Gradually

🔄 GitOps Principles
✔ Git = Source of Truth
✔ Declarative Infra
✔ Automated CI/CD
✔ Every change = Pull Request

🔒 Security Best Practices
🔐 Secrets
GitHub Secrets

AWS Secrets Manager

🛡 Container Security
Trivy Scan

Docker Bench Security

🔑 IAM Policy
Least privilege access

📊 Monitoring & Logging
Feature	Tool
Logs	CloudWatch / Fluent Bit
Metrics	Prometheus
Dashboards	Grafana
Alerts	Slack / Email

📜 Contributing
Fork the repo

Create a feature branch

Commit with proper message

Open Pull Request 🔥

🛠️ Author & Community
Project by Harshhaa
Let’s collaborate & make DevOps easy for everyone!

📧 Let's Connect
