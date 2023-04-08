Azure Infrastructure Operations Project: Deploying a scalable IaaS web server in Azure
Introduction
For this project, you will write a Packer template and a Terraform template to deploy a customizable, scalable web server in Azure.

Getting Started
Clone this repository

Create your infrastructure as code

Update this README to reflect how someone would use your code.

Dependencies
Create an Azure Account
Install the Azure command line interface
Install Packer
Install Terraform
Instructions
We will need to:

Create an Packer image.
Create infrastructure with Terraform template.
Packer Image
Run command to create packer image packer build server.json

Terraform Template
Implement code
Create a file main.tf to create
Create a file vars.tf to contain the variables
Initialize Terraform deployment
Run: terraform init to start
Terraform execution plan
Terraform plan command creates plan
Run: terraform plan -out solution.plan  The -out parameter allows specifying of the output file and review of the plan
Apply a Terraform plan
Terraform apply command to execute plan to infrastructure
Run: terraform apply solution.plan
How to customize vars.tf
Ex: If you want to deploy on other servers, you need to change values default in vars.tf file

  variable "server_names"{
  type = list
  default = ["<Server_1>","Server_2"]
}
Output
Terraform will perform: terraform out put
