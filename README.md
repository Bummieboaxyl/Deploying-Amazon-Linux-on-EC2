# Deploying-Amazon-Linux-on-EC2.


This project provides a step-by-step guide to launching a **Linux EC2 instance** on Amazon Web Services (AWS), using **Amazon Linux 2023**, which is ideal for cloud-based development and testing.

## 🐧 What Is Linux?

**Linux** is a free, open-source operating system known for its stability, security, and flexibility. It powers everything from web servers to IoT devices. **Amazon Linux** is a cloud-optimized distribution of Linux provided by AWS, tailored for performance and integration in EC2 environments.

### Prerequisites

- An AWS account
- An SSH client (e.g., Git Bash, PuTTY, MobaXterm)

### 🛠️ Steps to Deploy

 **Login to AWS Console**  
  - Go to [AWS Console](https://aws.amazon.com/console/) and open the EC2 Dashboard.

   - Click `Launch Instance` and select **Amazon Linux 2023** (Free Tier eligible).
![alt text](<images/Screenshot 2025-08-02 214823.png>)
![alt text](<images/Screenshot 2025-08-02 215114.png>)


 **Create Key Pair**  
   - Create a new key pair for SSH authentication.
   - Download the `.pem` file and store it securely on your computer.
![alt text](<images/Screenshot 2025-08-02 231802.png>)

 **Configure Security Group**  
   - Allow SSH (port 22) from Anywhere or limit it to your IP.
   - Name and save the security group.
   ![alt text](<images/Screenshot 2025-08-02 231916.png>)

 **Launch EC2**  
   Click the `Launch Instance` button and wait for the instance to initialize.

 **Status Check**  
   Wait a few minutes for AWS to complete its status checks.

## 🔗 Connecting to Your 
On your SSH client, navigate the the folder where your Private key pair is stored.
1. **Change Key Permissions**  
   ```bash
   chmod 400 keypairname.pem

- SSH Into Instance
Replace *keypairname.pem* and *PublicIPaddress* with your actual file and public IP:

*The default username for Amazon Linux is always ec2-user*

        ssh -i "keypairname.pem" ec2-user@PublicIPaddress

 ![alt text](<images/Screenshot 2025-08-02 233915.png>)       
- Login Successful
You’re now connected to your Linux server via SSH!
