Cyber Security Internship - Task 4  
Setup and Use a Firewall on Kali Linux Using UFW

---

Objective
Configure and test basic firewall rules to allow or block traffic on Kali Linux using **UFW (Uncomplicated Firewall)**.

---

Tools Used
- Kali Linux Terminal  
- UFW (Uncomplicated Firewall)  
- Telnet (for testing port blocking)  

---

## Step-by-Step Instructions with Commands

### 1. Check UFW Status
Check if UFW is active:
```bash

sudo ufw status

If inactive, enable it:

sudo ufw enable
 List Current Firewall Rules
List existing rules with numbering:

sudo ufw status numbered
 Block Inbound Traffic on Port 23 (Telnet)
Block Telnet (insecure) port 23:
sudo ufw deny 23
Verify the rule:
sudo ufw status numbered
Test Blocking of Port 23
Install Telnet client if not installed:


sudo apt install telnet
Try connecting to port 23:

telnet localhost 23
 Allow SSH (Port 22)
Allow SSH to keep remote access working:

sudo ufw allow 22
Verify rule addition:

sudo ufw status numbered
Remove the Block Rule on Port 23
Find the rule number for deny 23:


sudo ufw status numbered
sudo ufw delete number
Verify removal:

bash
Copy code
sudo ufw status
