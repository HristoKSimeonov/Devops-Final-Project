# Devops-Final-Project

Prerequisites
GitHub account
SSH keys generated and deployed to your GitHub account
Local machine with Terraform, Docker, Git, Jenkins, Kind, Kubectl, and Helm installed

Installation
1. Create a GitHub account if you don't have one already.

2. Generate SSH keys on your local machine.
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"

3. Deploy the public key to your GitHub account.
-Copy the public key to the clipboard.
cat ~/.ssh/id_rsa.pub
-Go to your GitHub account's settings and add the public key.

4. Clone the repository for your Python web application to your local machine.
git clone https://github.com/your-username/your-python-web-app.git

5.Change to the project directory.
cd your-python-web-app

6. Create the infrastructure using Terraform.
-Create a folder named terraform.
mkdir terraform
-Change to the terraform directory.
cd terraform
-Write the necessary Terraform configuration files (main.tf, variables.tf, etc.) to create an EC2 instance, security group, and ECR repository.
-Initialize Terraform.
terraform init
-Apply the Terraform configuration to create the infrastructure.
terraform apply
-Verify that the EC2 instance, security group, and ECR repository have been successfully created.

7. Configure the EC2 instance.
-Connect to the EC2 instance.
ssh -i /path/to/private/key.pem ec2-user@ec2-instance-ip
-Install the required tools (git, Jenkins, Docker, Kind, Kubectl, Helm) on the EC2 instance.
-Ensure the Jenkins user can access all of these tools.

8. Proceed with developing your Python web application using the Flask library.

9. Containerize your application by creating a Dockerfile.

10. Configure Jenkins to automate the deployment process.

11. Trigger the Jenkins pipeline to deploy your application to Kubernetes.


Acknowledgments
We would like to acknowledge the following resources and references that helped in the development of this project:

Flask Documentation:https://flask.palletsprojects.com/en/2.3.x/
Terraform Documentation:https://developer.hashicorp.com/terraform/docs
Docker Documentation:https://docs.docker.com/
Jenkins Documentation:https://www.jenkins.io/doc/
Kubernetes Documentation:https://kubernetes.io/docs/home/
AWS Documentation:https://docs.aws.amazon.com/

Contact
For any questions or feedback, please feel free to reach out to the project maintainer:

Maintainer Name: Hristo Simeonov
Maintainer GitHub: github.com/HristoKSimeonov
