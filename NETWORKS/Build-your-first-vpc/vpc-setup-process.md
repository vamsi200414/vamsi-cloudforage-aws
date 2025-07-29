# VPC Setup Process

This document outlines the step-by-step process to manually build a Virtual Private Cloud (VPC) in AWS using the Management Console. The goal is to create a basic networking setup including a VPC, subnet, and internet gateway.

---

## Architectural Diagram


<img width="919" height="734" alt="Screenshot 2025-07-29 190905" src="https://github.com/user-attachments/assets/999eb6f4-78b1-4d27-8508-e04f86a9b61f" />

---

## Step-by-Step Instructions

### Step 1: Log in to AWS Console

1. Navigate to [https://aws.amazon.com](https://aws.amazon.com) and log in to your AWS account.

**Why?**  
Access to the AWS Management Console is required to create and manage cloud resources.

---

### Step 2: Navigate to VPC Dashboard

2. In the AWS Management Console, search for **VPC** in the search bar.  
3. Click on **VPC** under "Services" to open the VPC Dashboard.

**Why?**  
The VPC Dashboard is the central place to manage all networking components like subnets, route tables, and internet gateways.

---

### Step 3: Create a Virtual Private Cloud

4. From the left-hand menu, click **Your VPCs**.  
5. Click **Create VPC**.  
6. Enter a name tag for your VPC (e.g., `my-first-vpc`).  
7. Under **IPv4 CIDR block**, choose `Manual input` and enter: `10.0.0.0/16`.  
8. Leave **IPv6 CIDR block** as `No IPv6 CIDR Block`.  
9. Click **Create VPC**.

**Why?**  
The VPC provides an isolated virtual network in the AWS cloud. The CIDR block defines the IP range that resources in the VPC can use.

---

### Step 4: Create a Subnet

10. In the left-hand menu, click **Subnets**.  
11. Click **Create subnet**.  
12. Enter a name for the subnet (e.g., `my-vpc-subnet`).  
13. Select the VPC you just created.  
14. Set the Subnet IPv4 CIDR block to `10.0.10.0/24`.  
15. Click **Create subnet**.

**Why?**  
Subnets divide the VPC into smaller sections and determine which range of IP addresses instances in the subnet will use.

---

### Step 5: Enable Auto-Assign Public IP

16. Select the subnet you created.  
17. Click **Actions** → **Edit subnet settings**.  
18. Enable **Auto-assign public IPv4 address**.  
19. Click **Save changes**.

**Why?**  
Enabling this ensures that any EC2 instance launched into this subnet receives a public IP, making it accessible from the internet (with the right configurations).

---

### Step 6: Create an Internet Gateway

20. In the left-hand menu, click **Internet Gateways**.  
21. Click **Create internet gateway**.  
22. Enter a name tag (e.g., `my-vpc-igw`) and click **Create internet gateway**.

**Why?**  
An internet gateway is needed to allow instances within the VPC to connect to the internet and to accept inbound internet traffic.

---

### Step 7: Attach Internet Gateway to VPC

23. Select the newly created internet gateway.  
24. Click **Actions** → **Attach to VPC**.  
25. Choose your VPC (`my-first-vpc`) and click **Attach**.

**Why?**  
Attaching the internet gateway to the VPC enables network traffic between the VPC and the internet.

---
