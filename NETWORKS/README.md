## Networking Fundamentals

---

### 1. What is Networking?  
**Answer:**  
Networking refers to the process of connecting multiple devices (such as computers, servers, and applications) to share resources and communicate with each other. In cloud computing, networking enables communication between different components hosted on the cloud, such as virtual machines, databases, and services.

---

### 2. Why Do We Need Networking?  
**Answer:**  
Networking is essential in cloud for:
- Enabling communication between resources  
- Managing traffic flow securely  
- Connecting cloud infrastructure with on-premises data centers  
- Allowing users to access applications over the internet

---

### 3. What is a VPC?  
**Answer:**  
A VPC (Virtual Private Cloud) is a logically isolated section of the cloud where you can launch and manage resources (like EC2 instances, databases) in a secure, virtual network that you define. You can control IP ranges, subnets, route tables, gateways, and more.

---

### 4. What Are Security Groups?  
**Answer:**  
Security Groups act as virtual firewalls for your cloud resources (like EC2 instances). They control inbound and outbound traffic at the instance level based on rules defined by protocol, port number, and source/destination IP.

---

### 5. What Do You Mean by NACLs?  
**Answer:**  
NACLs (Network Access Control Lists) are stateless firewalls that control traffic at the subnet level. They allow or deny specific inbound or outbound traffic using rules based on IP addresses, protocols, and ports.

---

### 6. Difference Between Security Group and NACL  

| Feature             | Security Group     | NACL                  |
|---------------------|--------------------|------------------------|
| Level               | Instance level      | Subnet level           |
| Stateful            | Yes                | No                     |
| Rule Evaluation     | All rules are evaluated | Rules evaluated in order |
| Direction           | Separate rules for inbound and outbound | Separate rules for inbound and outbound |
| Default Behavior    | Deny all inbound, allow all outbound | Allow all inbound and outbound |

---

### 7. What is a Subnet?  
**Answer:**  
A Subnet (Sub-network) is a range of IP addresses within a VPC. It allows you to group resources based on security and operational needs. You can create public or private subnets depending on the type of access required.

---

### 8. What is CIDR Range?  
**Answer:**  
CIDR (Classless Inter-Domain Routing) defines IP address ranges using notation like `10.0.0.0/16`. It helps define how many IPs a network/subnet can contain. For example, `/24` gives 256 IP addresses.

---

### 9. What is an Internet Gateway?  
**Answer:**  
An Internet Gateway (IGW) is a component that allows communication between resources in your VPC and the internet. It must be attached to the VPC and associated with a route table to enable internet access for public subnets.

---

### 10. What are Route Tables?  
**Answer:**  
Route Tables are sets of rules (routes) that determine where network traffic from your subnet or gateway is directed. Each subnet must be associated with a route table that defines how traffic should flow.

---

### 11. Difference Between Public and Private Subnet  

| Subnet Type   | Internet Access        | Use Case                    |
|---------------|------------------------|-----------------------------|
| Public Subnet | Yes (via IGW)          | Web servers, bastion hosts |
| Private Subnet| No direct internet access | Databases, internal services |

---

### 12. What is VPC Peering?  
**Answer:**  
VPC Peering is a networking connection between two VPCs that allows traffic to flow between them using private IP addresses. It enables resource sharing across accounts or regions without using public internet.

---
