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

**Docker Compose Web Deployment**

- Location: docker-compose/
- Description: A multi-container setup implementing automated isolated deployment layers to host web assets locally or across a distributed server network.
- Core Stack: Docker, Docker Compose (docker-compose.yaml), and custom HTML assets (index.html, main.html). Includes a GitHub Actions CI workflow (ci.yml).

**Kubernetes Declarative Pod Scaling**

- Location: kubernetes-pod-scaling/
- Description: Demonstrates native Kubernetes orchestration capabilities, featuring structured manifests for scaling application replicas, exposure management via services, and automated lifecycles.
- Core Stack: Kubernetes Manifests (deployment.yaml, service.yaml), Shell Scripting (delete-pod.sh), and GitHub Actions (k8s.yml).

**Linux Systems Administration Automation**

- Location: linux-syadmin-automation/
- Description: Contains production-ready utility scripts targeting standard systems engineering challenges, including target host health parsing and layout provisioning.
- Core Stack: Bash Shell Scripting (dir_struct.sh, health.sh) and Python 3 (app.py).

**Enterprise Terraform Hands-On**

- Location: terraform-hands-on/
- Description: A highly compliant Infrastructure as Code baseline mapping out declarative infrastructure state. Implements strict enterprise security parsing and programmatic code validation rules.
- Core Stack: HashiCorp Terraform (main.tf, variables.tf, providers.tf, outputs.tf). Enforces configurations via Checkov (.checkov.yaml) and TFLint (.tflint.hcl).

**Containerized Flask Application**

- Location: to-do-app-docker/
- Description: Focuses on microservice image building pipelines. Showcases clean image sizing strategies, caching optimization via dependency layer isolation, and runtime definitions.
- Core Stack: Python Flask (app.py, requirements.txt), Docker (Dockerfile), and .dockerignore patterns.