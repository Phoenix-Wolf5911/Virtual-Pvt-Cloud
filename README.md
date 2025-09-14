# 🌐 Virtual Private Cloud (VPC)

## 🔹 What is a VPC?
A **Virtual Private Cloud (VPC)** is a logically isolated section of a public cloud where you can run your resources securely.  
It behaves like your own private data center within AWS, giving you full control over **networking, IP ranges, routing, and gateways** — all while maintaining privacy from the public internet.

---

## 🎯 Purpose of a VPC
In AWS, a VPC lets you:
- Launch resources inside a secure and private environment.
- Customize your IP address range.
- Configure subnets, route tables, and gateways.
- Control inbound and outbound traffic with precision.

---

## 🚀 Why Choose Amazon VPC?
Amazon VPC removes the need for traditional hardware or VPNs and allows you to:
- Define and manage your networking environment entirely in the cloud.
- Control how your Amazon EC2 instances are accessed.
- Ensure granular security with fine-tuned access rules.
- Scale applications without worrying about on-prem infrastructure.

---

## 🛠️ Key Components of a VPC
- **VPC** → The private network environment you define.  
- **Subnets** → Logical partitions of your VPC for grouping resources.  
- **Internet Gateway (IGW)** → Enables connectivity between your VPC and the internet.  
- **NAT Gateway** → Lets private subnet resources access the internet securely.  
- **Virtual Private Gateway** → AWS side of a VPN connection.  
- **VPC Peering** → Private network link between two VPCs.  
- **VPC Endpoints** → Direct AWS service connectivity without public internet.  
- **Egress-only IGW** → IPv6 traffic outbound-only gateway.  

---

## 📝 How to Plan a VPC
1. Sign up for AWS & verify permissions.  
2. Choose IP address ranges (CIDR).  
3. Select Availability Zones.  
4. Plan subnetting (public & private).  
5. Design internet connectivity strategy.  
6. Create the VPC and deploy applications.  

---

## 📌 CIDR (Classless Inter-Domain Routing)
CIDR is a **flexible IP allocation system** that optimizes routing efficiency and reduces wastage.

- **Format** → IP + `/prefix` (e.g., `192.168.1.0/24`)  

**Advantages:**
- Reduces wasted IPs  
- Improves routing efficiency  
- Supports flexible supernetting  

**Classful Address Examples**
- Class A → `/8` → `44.0.0.1` → Large networks  
- Class B → `/16` → `128.16.0.2` → Medium networks  
- Class C → `/24` → `192.168.1.100` → Small networks  

---

## 🌍 VPC Addressing Options
- **IPv4 only** → VPC has just an IPv4 CIDR block.  
- **Dual Stack** → VPC supports both IPv4 and IPv6 CIDR blocks.  

---


---

## ⚙️ VPC Configuration Workflow

```markdown
## ⚙️ VPC Configuration Workflow

VPC (Name + CIDR + Tenancy)
   ↓
Availability Zones
   ↓
Subnets (Public & Private)
   ↓
Route Tables
   ↓
NAT Gateways (Private Subnets) → DNS Options (Enable DNS Hostnames + Resolution)
   ↓
Internet Gateway (Public Subnets) → DNS Options (Enable DNS Hostnames + Resolution)

