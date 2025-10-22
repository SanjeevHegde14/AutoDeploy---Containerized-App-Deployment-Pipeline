# AutoDeploy: Containerized-App-Deployment-Pipeline
Status: 🚧 Project in Progress 🚧

Project Goal

To build a complete, production-grade CI/CD pipeline for a containerized machine learning service. This project demonstrates modern DevOps best practices, from automated testing and containerization to orchestrated deployment on Kubernetes, bridging the gap between ML services and robust cloud infrastructure.

Planned Tech Stack

API Service: Python, FastAPI

Containerization: Docker

CI/CD Pipeline: GitHub Actions

Orchestration & Deployment: Kubernetes, Helm

Planned Architecture

CI (Continuous Integration): A GitHub Actions workflow will be triggered on every git push. The pipeline will automatically:

Install dependencies and run unit tests using pytest.

Build a new Docker image for the FastAPI application.

Push the tagged image to a container registry (e.g., GitHub Container Registry).

CD (Continuous Delivery): Upon successful completion of the CI stage, a second workflow will automatically deploy the new application version to a Kubernetes cluster by:

Checking out the project's Helm chart.

Executing a helm upgrade --install command to roll out the new container image with zero downtime.

This project will serve as a comprehensive demonstration of automating the lifecycle of a cloud-native application.
