# Create Amazon Linux Server in EC2 
Hello, in this project you are going to provide a step-by-step guide on creating and launching an Amazon Linux server in EC2 on AWS. EC2 is a fundamental service in the AWS ecosystem that provides resizable compute capacity in the cloud, enabling users to deploy and manage virtual servers with ease.
## Learning Objective
_Upon the complition of this project your are able to create Linux server using EC2 resources._
1. Launch virtual servers efficiently.
2. Configure secure network settings.
3. Manage cloud-based instances effectively.
4. Understand EC2 configurations comprehensively.
5. Develop cloud deployment expertise.
## Prerequisites
1. An active AWS account.
2. Basic knowledge of cloud computing concepts.
3. An SSH client Git for Linux/Mac.
# Step 1:- Login to the AWS Console
Login to your AWS account using your credentials.
# Step 2:- Deploy Server
_Amazon EC2 lets you create and manage resources as you define._ 
1. In the AWS management console search bar -search EC2 and click on the EC2 service.
2. Click on the 'Launch instance'(that is in the yellow box) 
#### Enter name of the server - Amazon-Linux_server
#### Select Amazon Machine Image from Quick start - Amazon Linux
#### Select Instance type - t2.micro
#### Next section is Key pair(login) 
    1. Click on -create new key pair
    2. Enter the Key pair name - Linux-key
    3. Select key pair type - RSA
    4. Select private key format - .pem
    5. Click on - create key pair
    6. Private key will be download on your local machine that is - Linux-key.pem
#### In Network setting you need to create 'security group' for SSH 
    1. Click on the check box of 'Allow SSH traffic from (anywhere - 0.0.0.0/0)'
#### Click on - Launch instance
# Step 3:- SSH Access of Server
- Open Git Bash on your local machine.
- For SSH need to enter path of the key.
- Eg. cd/e/aws/key 
- Using 'ls' command we can see our private key "Linux-key.pem". 
- After confirm path of the key.
- Go to the AWS console and click on the rescue instance.
- Click on 'connect'.
- Go to the 'SSH client' section.
- Copy the example - ssh -i "rescue-key.pem" ec2-user@ec2-x-x-x-x.us-west-1.compute.amazonaws.com
- Open Git on you local machine.
- Paste copied example on your Git Bash. 
- Then SSH authorize the key pair and after confirmation SSH successful.
# Summary
This project teaches the process of creating and managing an Amazon EC2 instance, covering instance configuration, secure network setup, SSH access, and basic server management. It equips learners with essential cloud computing skills to deploy and maintain virtual servers effectively on AWS.