# Kubernetes Application Deployment Exercise
## Overview
This exercise allowed the deployment of an Odoo application in a Minikube cluster using Kubernetes objects. The repository contains an Odoo application project and postgresSQL database. Run this application in a local Minikube environment.

## Submission
- [x] A fork of this repository has been created.
- [x] A `kubernetes` directory has been created in the project repository, and all Kubernetes YAML files have been placed there. Each resource includes a brief explanation in comments within the YAML files.


### Prerequisites

- Minikube installed and running
- kubectl configured to work with Minikube
- Basic understanding of Kubernetes concepts
- Docker installed (for building custom images if needed)

## Exercise Steps

- Clone the repository containing the Odoo application project.
- Create the following Kubernetes objects: a. Deployment for Odoo
    - Service to expose Odoo
    - ConfigMap for PostgreSQL configuration
    - Deployment for PostgreSQL
    - Ingress configured to make application able to be connected via HTTPS (Certificates are also needed here)
      - You will need to adapt `/etc/hosts` for the domain of your choice
    - Ensure your Kubernetes objects adhere to the following requirements:
      - Use the official Odoo image
      - Configure environment variables for database connection
      - Expose the Odoo service on a ClusterIP
      - Use a persistent volume for PostgreSQL data storage
    - Apply the Kubernetes objects to your Minikube cluster using kubectl apply -f <filename>.yaml.
    - Verify the deployment by accessing the Odoo application through the domain name