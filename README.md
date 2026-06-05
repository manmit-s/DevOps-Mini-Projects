
DevOps Mini Project
====================

Overview
--------

This repository contains a small collection of hands-on DevOps examples and exercises demonstrating common infrastructure and deployment techniques using Docker Compose, Kubernetes, and Terraform. Each subfolder is a focused demonstration that can be used independently to explore the respective technology.

Repository structure
--------------------

- docker-compose/: A minimal Docker Compose example and related Dockerfile and HTML demo.
 - docker-compose/: A minimal Docker Compose example and related Dockerfile and HTML demo.
- kubernetes-pod-scaling/: A simple Kubernetes deployment and service with a helper script for scaling and cleanup.
- terraform-hands-on/: Terraform configuration and example variables for provisioning infrastructure.
 - to-do-app-docker/: Dockerized to-do application with build and run instructions (see below).

Table of contents
-----------------

1. Quick start
2. Subproject details
3. Prerequisites
4. Usage examples
5. Testing and validation
6. Contributing
7. License and contact

Quick start
-----------

Choose the demonstration you want to run and follow the steps in the corresponding section below. Each example is intentionally small and self-contained so you can run it locally with minimal setup.

Subproject details
------------------

- docker-compose/
  - Purpose: Demonstrates building and running a simple multi-container application using Docker Compose.
  - Key files: docker-compose/docker-compose.yaml, docker-compose/Dockerfile, docker-compose/html/

- to-do-app-docker/
	- Purpose: A containerized to-do application demonstrating Dockerfile best practices and a simple web frontend/backend setup.
	- Key files: to-do-app-docker/Dockerfile, to-do-app-docker/docker-compose.yaml, to-do-app-docker/README.md
	- Quick run:

		cd to-do-app-docker
		docker-compose up --build -d

		# then visit the app on the configured port (see to-do-app-docker/README.md)

- kubernetes-pod-scaling/
  - Purpose: Demonstrates a Kubernetes Deployment, Service, and a small script to delete pods or scale the deployment.
  - Key files: kubernetes-pod-scaling/deployment.yaml, kubernetes-pod-scaling/service.yaml, kubernetes-pod-scaling/delete-pod.sh

- terraform-hands-on/
  - Purpose: Example Terraform configuration showing providers, variables, and outputs for simple infrastructure provisioning.
  - Key files: terraform-hands-on/main.tf, terraform-hands-on/variables.tf, terraform-hands-on/terraform.tfvars

Prerequisites
-------------

- Docker (for the Docker Compose example)
- Docker Compose (v1.27+ or Docker Compose v2)
- kubectl and a Kubernetes cluster (minikube, kind, or remote cluster) for the Kubernetes example
- Terraform (v1.0+) for the Terraform example

Usage examples
--------------

Docker Compose

1. Change directory to the Docker Compose example:

	cd docker-compose

2. Build and start the services:

	docker-compose -f docker-compose.yaml up --build -d

3. To stop and remove the containers:

	docker-compose -f docker-compose.yaml down

Kubernetes (local cluster)

1. Apply the Kubernetes manifests:

	kubectl apply -f kubernetes-pod-scaling/deployment.yaml
	kubectl apply -f kubernetes-pod-scaling/service.yaml

2. Verify the deployment and service:

	kubectl get deployments
	kubectl get pods
	kubectl get services

3. Scale the deployment (example):

	kubectl scale deployment <deployment-name> --replicas=3

4. The repository includes `kubernetes-pod-scaling/delete-pod.sh` for a small scripted cleanup helper.

Terraform

1. Initialize Terraform in the Terraform folder:

	cd terraform-hands-on
	terraform init

2. Review the plan and apply (example with variables file):

	terraform plan -var-file=terraform.tfvars
	terraform apply -var-file=terraform.tfvars

3. When finished, destroy the created resources:

	terraform destroy -var-file=terraform.tfvars

Testing and validation
----------------------

- For Docker Compose: confirm containers are running using `docker ps` and visit the demo endpoints in a browser if the services expose HTTP ports.
- For Kubernetes: use `kubectl describe` and `kubectl logs` to inspect pod status and logs; use `kubectl get` commands to validate resources.
- For Terraform: validate by reviewing the planned changes and by checking the provider's console or API for created resources.

Contributing
------------

Contributions are welcome. Keep changes focused and self-contained. For larger additions, open an issue describing the proposal before submitting a pull request.

When contributing:

- Add a short description of the change in the pull request.
- Ensure examples remain minimal and easy to run locally.

License and contact
-------------------

This repository does not include an explicit open-source license. If you intend to reuse the content, add a LICENSE file or contact the repository owner to clarify terms.

For questions or suggestions, open an issue in this repository.

