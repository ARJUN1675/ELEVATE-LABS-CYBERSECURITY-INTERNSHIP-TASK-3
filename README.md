# ELEVATE-LABS-CYBERSECURITY-INTERNSHIP-TASK-3

# Basic Vulnerability Scan using Nessus Essentials

Task Overview
This task demonstrates a **basic vulnerability scan** performed on my local Windows machine using **Nessus Essentials**.  
The objective was to identify potential security issues, review their severity, and document possible mitigations.

Tools Used
- **Nessus Essentials (Free Edition by Tenable)**
- Windows 10/11 (Localhost Target)

## Steps Followed

### 1. Install Nessus Essentials
- Downloaded and installed **Nessus Essentials** on Windows from [Tenable](https://www.tenable.com/products/nessus/nessus-essentials).
- Activated using a free license key provided by email.

---

### 2. Set up scan target as your local machine IP or localhost
- Target used: **192.168.29.28 (Localhost)**

---

### 3. Start a full vulnerability scan
- Performed two scans:
  - **Host Discovery Scan**
  - **Basic Network Scan**

---

### 4. Wait for scan to complete (may take 30–60 mins)
- Host Discovery Scan completed in ~3 minutes.  
- Basic Network Scan completed in ~8 minutes.  

---

### 5. Review the report for vulnerabilities and severity
**Host Discovery Scan Results:**
  - 🔴 Critical: 0  
  - 🟠 High: 0  
  - 🟡 Medium: 0  
  - 🟢 Low: 0  
  - 🔵 Info: 2

**Basic Network Scan Results:**
  - 🔴 Critical: 0  
  - 🟠 High: 0  
  - 🟡 Medium: 2  
  - 🟢 Low: 0  
  - 🔵 Info: 31  
  - **Total Findings: 33**

---

### 6. Research simple fixes or mitigations for found vulnerabilities
- **SSL Certificate Cannot Be Trusted**  
  - Install a valid SSL/TLS certificate signed by a trusted Certificate Authority.  
- **SMB Signing Not Required**  
  - Enable SMB signing in Windows Group Policy to prevent man-in-the-middle attacks.  

---

### 7. Document the most critical vulnerabilities
**Top Vulnerabilities:**  
  1. **SSL Certificate Cannot Be Trusted** *(Medium, CVSS 6.5)*  
     - Risk: The certificate presented cannot be trusted, may allow MITM attacks.  
     - Fix: Install a valid certificate signed by a trusted CA.  
  2. **SMB Signing Not Required** *(Medium, CVSS 5.3)*  
     - Risk: Could allow man-in-the-middle attacks on SMB traffic.  
     - Fix: Enable SMB signing in Windows Group Policy.    

---

## Reports
- [My Host Discovery Scan PDF]
- [My Basic Network Scan PDF] 

---

Mitigation Recommendations
- Apply latest **Windows Updates** and security patches.  
- Replace or update **SSL/TLS certificates** with trusted ones.  
- Enable **SMB signing** and disable legacy SMBv1.  
- Keep firewall and antivirus enabled.  
- Remove/disable unnecessary services.

---

Conclusion
The scans revealed **no critical or high vulnerabilities**, but identified **medium-severity risks** related to SSL certificates and SMB configuration.  
By applying recommended fixes, the overall security posture of the system can be improved.

---
