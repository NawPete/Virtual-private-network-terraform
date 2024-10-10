# Cloud Infrastructure with Terraform

### This project utilizes Terraform to manage cloud infrastructure, allowing for the automated creation and configuration of resources. The project is organized into modules, which enhances modularity and ease of management for different infrastructure components.
Modules

### The project includes the following modules, each responsible for a specific part of the infrastructure:

#### Alb (Application Load Balancer)
The ALB module manages the configuration of an Application Load Balancer, enabling incoming traffic distribution across multiple instances.
Files in the module:
- main.tf: Defines resources for the ALB.
- outputs.tf: Specifies outputs that export values for use in other parts of the infrastructure.
- variables.tf: Input variables that allow customization of the ALB configuration.

#### EC2 (EC2 Instances)
The EC2 module manages the configuration of EC2 instances, which are virtual machines hosting applications.
Files in the module:
- data.tf: Defines data sources that reference existing resources.
- main.tf: Contains EC2 resource definitions.
- outputs.tf: Exports values related to EC2.
- variables.tf: Contains variables for flexible configuration of EC2 instances.

#### SG (Security Groups)
The SG module manages security groups, which control incoming and outgoing traffic to cloud resources.
Files in the module:
- main.tf: Defines the Security Group resources.
- outputs.tf: Exports values related to the Security Group.
- variables.tf: Contains variables to customize traffic rules within the Security Group.

#### VPC (Virtual Private Cloud)
The VPC module creates and configures a Virtual Private Cloud (VPC), providing network isolation and control in the cloud environment.
Files in the module:
- main.tf: Contains VPC resource definitions, such as subnets, route tables, and other networking resources.

### Main Files

### The project’s main directory includes the following Terraform files:

- main.tf: The main Terraform file, which integrates modules and orchestrates their deployment.
- provider.tf: Cloud provider configuration, specifying the cloud environment where resources will be deployed (e.g., AWS).
- terraform.tfvars: A variables file that defines specific values for variables used across the modules, allowing for infrastructure customization.
- variables.tf: Variable definitions used throughout the project, enabling flexibility and configurability.

#### This Terraform project simplifies cloud infrastructure management in a modular and automated manner, enabling rapid deployment, resource scaling, and configuration adjustments tailored to application needs.
