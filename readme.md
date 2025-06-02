## 🚀 Deploy a Linux Server on AWS EC2

Welcome to this hands-on project where you'll learn to **create and manage a Linux server** using **Amazon EC2**, one of AWS’s most essential services for deploying scalable cloud infrastructure.

---

### 🎯 Learning Objectives

By completing this project, you’ll be able to:

* ✅ Launch a virtual Linux server (Amazon Linux or Ubuntu)
* ✅ Configure secure network settings (Security Groups)
* ✅ Connect via SSH using key pairs
* ✅ Understand EC2 instance configurations
* ✅ Build real-world skills in cloud deployment & management

---

### 📚 Prerequisites

Before starting, make sure you have:

* 🔐 An **active AWS account**
* ☁️ Basic understanding of **cloud computing**
* 💻 An **SSH client** like Git Bash 
* 🌐 Stable internet connection

---

### 🛠️ Step-by-Step Guide

#### 1️⃣ Login to AWS Console

1. Visit [https://aws.amazon.com](https://aws.amazon.com)
2. Log in using your AWS account credentials

---

#### 2️⃣ Launch the EC2 Instance

1. In the AWS Console search bar, type `EC2`
2. Click on **EC2** under Services
3. Click **Launch instance**

##### 📝 Configure Instance Settings:

* **Name**: `Linux_Server`
* **Amazon Machine Image (AMI)**: Choose one of the following from Quick Start:

  * 🐧 **Amazon Linux** *(Free Tier Eligible)* \
  * 🧊 **Ubuntu Server** *(Free Tier Eligible)*
* **Instance Type**:
  Select `t2.micro` *(Free Tier eligible)*

---

#### 3️⃣ Create a Key Pair 🔐

To enable secure SSH access:

1. Under **Key pair (login)**, click `Create new key pair`
2. Enter a name: `<Key-Name>`
3. Key pair type: `RSA`
4. Private key format: `.pem`
5. Click `Create key pair`
6. The file `<Key-Name>.pem` will be downloaded — **save this securely**

---

#### 4️⃣ Configure Network Settings 🌐

Set up inbound rules to allow SSH access:

1. Scroll to **Network settings**
2. Under **Firewall (Security Group)**:

   * ✅ Check `Allow SSH traffic from` and choose `Anywhere (0.0.0.0/0)`

     > ⚠️ Later, restrict this to **My IP** for better security.

_Note:- This network setting is for SSH purpose Your can add more Inbound rule as per your requirement._

---

#### 5️⃣ Launch the Instance 🚀

Click on **Launch Instance**

* 🕒 Wait a few moments for the instance to move into `Running` state.
* 📋 Note the **Public IPv4 address** or **Public DNS**.

---

### 6️⃣: Connect to Your Server via SSH 🔌

#### 🖥️ Use Git Bash or Terminal

1. Open **Git Bash** or Terminal on your machine

2. Navigate to the directory where the `.pem` file is saved:

```bash
     cd /path/to/your/key
     ls                  #Verify your private key (.pem file)
```

3. Modify permissions (required by SSH):

```bash
     chmod 400 Linux-key.pem
```

4. Go back to your EC2 instance in AWS Console:

   * Click **Connect**
   * Go to the **SSH Client** tab
   * Copy the provided `ssh` command, which looks like:

   For Amazon Linux:

```bash
     ssh -i "Linux-key.pem" ec2-user@<your-public-ip>
```

   For Ubuntu:

```bash
   ssh -i "Linux-key.pem" ubuntu@<your-public-ip>
```

5. Paste and run the command in Git Bash or Terminal.

✅ You're now logged in to your Linux server hosted on AWS EC2!

---

### Summary 🎉

You’ve successfully:

* 🐧 Launched a Linux EC2 instance (Amazon Linux or Ubuntu)
* 🔐 Created and used a key pair for secure access
* 🌐 Configured network access via Security Groups
* 📡 Connected to your cloud-hosted Linux server via SSH

This foundational skill will help you in future projects involving server setup, software installation, DevOps, and cloud automation.

---

### 💡 Pro Tips

* 🔐 Replace `Anywhere (0.0.0.0/0)` with `My IP` in SSH rules for security
* 📦 Install software using:

  * `sudo yum update` for Amazon Linux
  * `sudo apt update` for Ubuntu
  * `sudo yum install <package_name>` for Amazon Linux
  * `sudo apt install <package_name>` for Ubuntu

* 🔄 Public IP may change if you stop/start the instance — use **Elastic IP** for a static address.

---

### 📬 Need Help?

Explore more:

* 📖 [AWS EC2 Docs](https://docs.aws.amazon.com/ec2/)

---

Happy Cloud Building! ☁️🐧🚀
**\~ With Avinash Jagtap**

---
