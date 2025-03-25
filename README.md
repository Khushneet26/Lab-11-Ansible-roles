# Lab 11 - Ansible Roles

## Setup Instructions

### Clone the Repository
```bash
git clone https://gitlab.com/cit_4640/4640-w11-lab-start-w25.git
cd 4640-w11-lab-start-w25
```

### Generate a New SSH Key for AWS
```bash
ssh-keygen -t rsa -b 4096 -f ~/.ssh/aws
```

### Add the SSH Key to AWS
Run the provided scripts to add the SSH key to your AWS account.

### Initialize Terraform and Create Servers
```bash
cd terraform
terraform init
terraform apply -auto-approve
```
This will create two servers: one running Ubuntu and the other running Rocky Linux.

## Ansible Configuration

### Check Dynamic Inventory
```bash
cd ansible
ansible-inventory -i inventory/aws_ec2.yml --list
```

### Run the Playbook
```bash
ansible-playbook -i inventory/aws_ec2.yml playbook.yml
```

### Verify Nginx on Frontend Server
Open a browser and navigate to the public IP of your Ubuntu server to see the deployed HTML page.

## Git Commands for Submission

### Initialize Git (if not already initialized)
```bash
git init
```

### Set Up Remote Repository (if needed)
```bash
git remote remove origin # Remove old remote if necessary
git remote add origin git@github.com:Khushneet26/Lab-11-Ansible-roles.git
```

### Push Code to GitHub
```bash
git add .
git commit -m "Initial commit with Ansible roles"
git push -u origin main
```

