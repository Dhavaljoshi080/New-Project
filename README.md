# New-Project

## How to write readme.md file
https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project

## Initial set up for project using Terraform
   - Clone the GitHub to the local machine ( overview to push and pull files from GitHub -  https://www.onlinetutorialspoint.com/git/step-by-step-how-to-push-the-project-into-git-repository.html )
  
   - Created New-Project Repo on GitHub - https://github.com/Dhavaljoshi080/New-Project.git
   
   - Created New-Project/ Terrafrom_config/
   
   - Installed Terraform from - https://learn.hashicorp.com/tutorials/terraform/install-cli
   
   - Installed AWS CLI - for Authentication by credential (to make it secure so we don’t have to put credentials in .tf file as plain text
                      https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
   
   - Created IAM users - https://us-east-1.console.aws.amazon.com/iam/home#/users$new?step=final&accessKey&userNames=Nishant&userNames=Dhaval&userNames=Faisal&userNames=Gagan&permissionType=policies&policies=arn:aws:iam::aws:policy%2FAdministratorAccess
```
$ aws configure --profile DJ-AWS
```

- Give  give credentials given to you access id and  key 

- Created code for terraform
- vim main.tf
- vim variable.tf
- vim sg.tf
- Pushed it to gitHub
```
$ Terraform init
$ Terraform plan
$ Terraform apply
```

It will create a security group and ec-2 instance

Management master VM
Management  VPC
- VPC: vpc-0a456cfb0dd41261b
- Subnet: subnet-01005b844b3dc722b    
- Availability Zone = us-east-2a
- AMI: ami-008e1e7f1fcbe9b80 


# created Production load Instances 
Pushed Terraform code to GitHub and applied to create  2 instances and a security group

Load VPC 
- VPC id: vpc-0fdf778d69038751e 
- Availability Zone =ca-central-1a 
- Subnet id: subnet-03ddbe0583ca7bd8e 
- AMI: ami-041d49677629acc40
