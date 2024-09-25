### GitOps Automation for Kubernetes Deployment
This project automates infrastructure provisioning and application deployment using GitHub Actions, Terraform, and AWS cloud services.

### Key Components:
### GitHub Actions: Used for CI/CD workflows that handle both infrastructure (using Terraform) and application build, test, and deployment.

### Terraform Workflow:
Fetches the stage branch for planning and testing.
Merges pull requests into the main branch for final deployment.
Applies changes using Terraform to manage AWS EKS and VPC infrastructure.
Build, Test & Deploy Workflow:
Uses Maven for code building and testing.
Docker is employed for containerization.
Deploys the containers to AWS EKS using Helm charts.
Stores container images in Amazon ECR (Elastic Container Registry).
Code Quality: SonarCloud is integrated into the CI/CD pipeline for code quality checks and analysis.

### Flow:
Developers push code to a branch in GitHub.
GitHub Actions triggers the Terraform workflow to plan and apply infrastructure changes.
The application code is built, tested using Maven, containerized via Docker, and deployed to EKS.
Helm charts manage the Kubernetes deployments.
SonarCloud performs static code analysis to ensure high code quality.

### Tools & Technologies:
### Terraform: Infrastructure as Code (IaC) tool for managing AWS resources like EKS and VPC.
### Helm: Kubernetes package manager used to deploy applications on EKS.
### Maven: Build automation tool used for compiling and testing Java projects.
### Docker: Containerization technology used to package the application for deployment.
### AWS ECR: Stores container images that are deployed to AWS EKS.
### SonarCloud: Monitors and reports on code quality and security vulnerabilities.