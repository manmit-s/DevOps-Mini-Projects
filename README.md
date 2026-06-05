# DevOps Mini Projects

## Description
A curated collection of production-ready DevOps mini-projects demonstrating modern infrastructure practices. This repository serves as a practical guide for containerization, orchestration, infrastructure as code (IaC), and system administration automation. Each module contains localized configurations and automated workflows to ensure isolated testing and deployment.

---

## Repository Structure

The repository is organized into distinct project directories based on technology stack and use case:

*   **`docker-compose/`** — Multi-container application orchestration leveraging Docker Compose for local environment replication.
*   **`kubernetes-pod-scaling/`** — Kubernetes manifests and automation scripts demonstrating horizontal pod autoscaling and resilience.
*   **`linux-sysadmin-automation/`** — Native Bash and Python utility scripts engineered to automate system health checks and directory tree visualization.
*   **`terraform-hands-on/`** — Declarative infrastructure blueprints utilizing HashiCorp Terraform alongside automated linting (`tflint`) and security compliance tools (`checkov`).
*   **`to-do-app-docker/`** — A lightweight, containerized Flask application featuring optimized multi-stage build patterns.

---

## Core Technologies

*   **Containerization & Orchestration:** Docker, Docker Compose, Kubernetes
*   **Infrastructure as Code:** HashiCorp Terraform
*   **Automation Languages:** Python, Bash Shell Scripting
*   **Quality Assurance & Security:** Checkov, TFLint, GitHub Actions CI/CD

---

## Project Modules and Deployment

### 1. Containerized To-Do Application (`to-do-app-docker/`)
A basic Python Flask application configured to execute within an isolated container runtime environment.

**Deployment Steps:**
1. Navigate to the project directory:
```bash
   cd to-do-app-docker