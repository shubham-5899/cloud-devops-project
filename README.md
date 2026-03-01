# End-to-End CI/CD Pipeline with Jenkins, Docker & AWS

This project demonstrates a complete CI/CD pipeline that automatically builds,
pushes, and deploys a Dockerized Node.js application to AWS EC2 using Jenkins.

The pipeline performs:
- Code checkout from GitHub
- Docker image build
- Push to DockerHub
- Automated deployment to EC2

## Tech Stack

- Jenkins (CI/CD)
- Docker (Containerization)
- DockerHub (Image Registry)
- AWS EC2 (Deployment Server)
- GitHub (Source Code Management)


## Pipeline Stages

1. Checkout Code
2. Build Docker Image
3. Login to DockerHub
4. Push Image
5. Pull Latest Image on EC2
6. Restart Container


## Run Locally

docker build -t devops-app .
docker run -p 3000:3000 devops-app

## Future Improvements

- Infrastructure provisioning using Terraform
- Migration to Kubernetes
- SSL setup with Nginx
- Monitoring with Prometheus


<img width="959" height="361" alt="Screenshot 2026-03-01 185821" src="https://github.com/user-attachments/assets/ea95e2dc-f67e-4d3e-b5b3-f7b5759d5fc1" />
<img width="960" height="355" alt="Screenshot 2026-03-01 190348" src="https://github.com/user-attachments/assets/58718b36-4ffa-4bd5-b904-f85881e9e99d" />
<img width="960" height="393" alt="Screenshot 2026-03-01 190430" src="https://github.com/user-attachments/assets/348b9b2d-8945-4513-b135-ff25993f62fe" />
<img width="944" height="474" alt="Screenshot 2026-03-01 190310" src="https://github.com/user-attachments/assets/a43569d7-e92d-4511-8d83-76775100bcfc" />
<img width="948" height="417" alt="Screenshot 2026-03-01 190846" src="https://github.com/user-attachments/assets/2ad914bc-5210-479c-a36c-c358d68cb2da" />
<img width="1320" height="98" alt="Screenshot 2026-03-01 232013" src="https://github.com/user-attachments/assets/0e7f1a75-b3f9-4c07-9e2d-c95ed279e3ae" />





