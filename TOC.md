# Table of Content

## Branches

- 02_02 - using input variables
  - `environment = var.environment_map[var.target_environment]` 
    - -var="target_environment=DEV"
- 02_06 - for_each
  ```sh
  variable "environment_list" {
    type = list(string)
    default = ["DEV","QA","STAGE","PROD"]
  }

  for_each = toset(var.environment_list)
  name = "${lower(each.key)}_${var.project-id}"
  ```

## Contents
 
1. Creating a New Terraform Configuration
  - Practical Terraform
  - Google Cloud and Terraform: Tools and setup
  - Designing a cloud infrastructure in Terraform
  - Terraform configuration overview
  - Deploying the Terraform configuration
  - Review deployed resources
  - Destroying resources
  
2. Intermediate Terraform Concepts
  - Input variables
  - Using input variables
  - Output variables
  - Sensitive data
  - Looping with count
  - Looping with for_each
  - Expressions and functions
  - Introduction to modules
  - Using Terraform modules

3. Advanced Terraform Concepts
  - Analyzing a module
  - Custom modules
  - Terraform remote state overview
  - Deploying backend resources
  - Deploying a remote state configuration
  
4. Terraform Automation
  - Multiple environment configurations
  - Terraform CI/CD options
  - Terraform Cloud setup
  - Deploying with Terraform Cloud
  - GitOps CI/CD setup
  - GitOps CI/CD with Terraform Cloud
  - Deprecating resources
  