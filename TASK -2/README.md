# OASIS INFOBYTE INTERNSHIP  
**Task 2: Basic Firewall Setup with UFW**  

**Prepared by:** Jaideep Raj Dutta  
**Date:** August 2025  

---

## Environment
- OS: Kali Linux (Virtual Machine)  
- Tool: UFW (Uncomplicated Firewall)  

---

## Objective
For this task, I had to set up a basic firewall on my Kali Linux VM using UFW.  
The idea was to allow only the traffic I actually need and block the rest for better security.

---

## Steps I Did

1. **Update and Install UFW**
   ```bash
   sudo apt update
   sudo apt install ufw

2. **Enable UFW**
   ```bash
   sudo ufw enable

3. **Set Default Rules**
Block all incoming traffic and allow all outgoing traffic:
   ```bash
   sudo ufw default deny incoming
   sudo ufw default allow outgoing

4. **Allow Required Ports**

- SSH (Port 22)
   ```bash
   sudo ufw allow 22/tcp

- HTTP (Port 80)
   ```bash
   sudo ufw allow 80/tcp

5. **Check Status**
   ```bash
   sudo ufw status verbose

---

**Files Included in This Repository**
- **ufw_configuration.txt** – Terminal output of commands  
- **README.md** – This documentation  

---

**Tools & Resources**
- [UFW Official Documentation](https://help.ubuntu.com/community/UFW)  
- Kali Linux Documentation  

---

**Prepared by:** Jaideep Raj Dutta 
**Date:** August 2025   

## Sample Output

   ```bash
   Status: active

   To                         Action      From
   --                         ------      ----
   22/tcp                     ALLOW       Anywhere
   80/tcp                     ALLOW       Anywhere
   22/tcp (v6)                ALLOW       Anywhere (v6)
   80/tcp (v6)                ALLOW       Anywhere (v6)




