🚀 PHP Laravel DevOps Deployment (AWS + Docker + GitLab CI/CD)

This project demonstrates a production-style DevOps deployment of a Laravel application on AWS EC2 (Amazon Linux) using Docker, Nginx, and a Self-Hosted GitLab Runner.
The entire pipeline automates build, test, and deployment with zero manual server login.

## 🔧 Tech Stack
- PHP (Laravel Framework)
- Amazon Linux EC2 (Free Tier)
- Docker & Docker Compose
- Nginx Reverse Proxy
- GitLab CI/CD (Self-Hosted Runner on EC2)
- Amazon S3 (optional for assets/storage)
- Cloudflare DNS (optional for domain + SSL)

## 📦 Architecture

**Developer → Push Code → GitLab → CI/CD Pipeline → EC2 → Docker Containers → Nginx → Live App**

- Laravel runs inside PHP-FPM container
- Nginx routes incoming traffic to Laravel container
- Docker Compose manages multi-container setup
- GitLab Runner installed on EC2 automates deployment
- Pipeline deploys without manual SSH login

🔁 CI/CD Flow

- Developer pushes code to main branch
- GitLab CI/CD pipeline automatically triggers
- Docker image is built on Amazon Linux
- Old containers stop → new ones deploy
- Database migrations (if configured) run automatically
- Application update goes live instantly

📦 Infrastructure Overview
Component	    Technology
Compute         AWS EC2 (Amazon Linux)
Web Server	    Docker + Nginx
App Runtime 	Laravel on PHP-FPM
Automation	    GitLab CI/CD Runner
Reverse Proxy	Nginx
SSL (optional)	Let's Encrypt via Cloudflare

## 📸 CI/CD & Deployment Proof

### GitLab Pipeline Success
![Pipeline](screenshots/pipeline-success.png)

### Deployment Job
![Deploy](screenshots/pipeline-deploy.png)

### Laravel Application UI
![Laravel UI](screenshots/laravel-ui.png)

### Docker Containers
![Docker PS](screenshots/docker-ps.png)

### GitLab Runner
![Runner](screenshots/gitlab-runner.png)
