# Project: Windows Server 2022 Active Directory Deployment

## 📌 Overview
This project documents the deployment of a new Domain Controller in a virtualized environment. The goal was to establish a foundational identity infrastructure using **Active Directory Domain Services (AD DS)** and **DNS**.

## 🛠️ Technical Stack
* **Hypervisor:** VMware Workstation
* **OS:** Windows Server 2022
* **Network:** Static IP Configuration (Subnet: 192.168.10.0/24)
* **Roles:** Domain Controller, DNS Server

## 📸 Implementation Steps

### Step 1: Network Configuration
The server was configured with a Static IP (`192.168.10.2`) to ensure reliable reachability for domain clients.
![Static IP Config](01-static-ip-config.png)

### Step 2: Role Installation
Installed the **Active Directory Domain Services (AD DS)** role via the Server Manager wizard.
![AD DS Selection](02-adds-role-selection.png)

### Step 3: Domain Promotion (New Forest)
Promoted the server to a Domain Controller. I created a new forest root domain named **`NMA.local`** (or the name visible in your screenshot).
![New Forest Setup](03-promote-new-forest.png)

### Step 4: NetBIOS Configuration
Verified the NetBIOS domain name to ensure compatibility with older legacy systems on the network.
![NetBIOS Config](04-netbios-config.png)

### Step 5: Prerequisites & Installation
Successfully passed all prerequisite checks, confirming the server environment (OS patch level, Administrator password) was compliant before finalizing the installation.
![Prerequisites Check](05-prerequisites-check.png)

### Step 6: Verification & Tools
After the restart, the Server Manager Dashboard confirmed that **AD DS** and **DNS** services are active (green).
![Dashboard Verification](06-server-manager-dashboard.png)

I also verified that the administrative tools, including **Active Directory Users and Computers**, were successfully installed and ready for user management.
![AD Tools](07-ad-tools-menu.png)

## ✅ Final Outcome
The server is now fully operational as the Primary Domain Controller for the `NMA.local` domain. I have successfully:
1. Configured the Network Layer (Static IP).
2. Deployed the Identity Layer (AD DS).
3. Validated the Management Layer (AD Tools).
