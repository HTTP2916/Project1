# Azure Infrastructure Operations: Deploying a Web Server in Azure

## Introduction
For this project, we customize Packer template and a Terraform template to aim at deploying a Web Server in Azure.

## Dependencies
+ An Azure account
+ Packer template
+ Terraform template

## Instructions
### Create Image Packer
- File: packer/server.json
- Use command to create image for virtual machine
``` packer build packer/server.json ```

### Terraform Template
Create infrastructure with Terraform template.
- File: main.tf => declare the resouces
- File: vars.tf => declare variable

Use some command below to init and deploy terraform
- Get started
``` terraform init ```

- Initialize a directory containing Terraform
``` terraform plan [option] ```

- Save the plan solutions file use this command
``` terraform plan -out solutions.plan ```

- Deploy terraform infrastructure
``` terraform apply "solutions.plan" or terraform apply main.tf ```

### Customize vars.tf
This file contains all the variables used inside the terraform/main.tf. If you want to deploy on other servers, you need to change values default inside the file.
  variable "server_names"{
  type = list
  default = ["<Server_1>","Server_2"]
}
### Output
Azure login

![az login](https://user-images.githubusercontent.com/50509460/230714172-c57ae202-d396-49df-b47e-96c04258bed1.PNG)

Packer Build

![packer build](https://user-images.githubusercontent.com/50509460/230714193-6a9b5e1e-6d1c-4fb6-946a-9d54ff2eb2d0.PNG)

Init Terraform

![terraform init](https://user-images.githubusercontent.com/50509460/230714264-8abb9dc9-b00a-4609-bd02-f517106c979b.PNG)

Terraform Plan out

![terraform plan out](https://user-images.githubusercontent.com/50509460/230714295-101bdb93-04bd-474c-b3e2-e07240691ebc.PNG)

Terraform apply solution

![terraform apply solution](https://user-images.githubusercontent.com/50509460/230714314-bb8e8c94-3031-4c32-b8fe-3f0e256528ab.PNG)

Terraform will perform: terraform out put

![output](https://user-images.githubusercontent.com/50509460/230714150-2d6b2682-1996-40b8-a866-6c4c5d701dea.PNG)

