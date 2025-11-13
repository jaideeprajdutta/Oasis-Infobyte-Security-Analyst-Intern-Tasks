# OASIS-INFOBYTE-INTERNSHIP  
## Task 1: Basic Network Scanning with Nmap  

### Environment  
- Operating System: Kali Linux (Virtual Machine)  
- Tool Used: Nmap Version 7.95  

### Objective  
Perform a network scan on a target IP address to identify open ports and services. Document the results and explain the significance of each open port.

### Steps Performed  
1. Updated Kali Linux packages and installed Nmap.  
2. Ran the command: nmap -sV 192.168.8.129
(Replace 192.168.8.129 with the IP address of the target machine.)  
3. Saved the scan output to a file named `nmap_scan_results.txt`.  
4. Analyzed the scan results and documented the findings.
nmap -sV 192.168.8.129 > nmap_scan_results.txt

### Scan Findings  
- The target IP (e.g., 192.168.8.129) was up and reachable.  
- [Describe here the open ports and services, or state if no open ports found.]  
- Example:  
- Port 22 (SSH): Secure remote login service.  
- Port 80 (HTTP): Web server service.

### Significance of Open Ports  
- Open ports indicate accessible services that might be available for communication or potentially vulnerable to attacks.  
- Properly managing open ports helps reduce attack surface.

### Files Included in This Repository  
- `nmap_scan_results.txt` — Contains the detailed scan output and analysis.  
- `README.md` — This file, describing the project and results.

### Tools & Resources  
- [Nmap Official Website](https://nmap.org)  
- Kali Linux Documentation  

---

*Prepared by:* S Jaideep Raj Dutta  
*Date:* 01 August 2025  
