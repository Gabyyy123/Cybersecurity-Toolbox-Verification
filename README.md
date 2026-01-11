# Cybersecurity-Toolbox-Verification
Setup, auditing, and verification of a professional penetration testing environment.


##  Overview
This project documents the installation, configuration, and auditing of my professional security lab. As a BSIT student, I prioritize **Technical Discipline** by ensuring every tool in my arsenal is verified, up-to-date, and functional within an isolated environment.

---

##  Lab Architecture
To maintain a secure boundary between my testing tools and personal data, I utilize a hybrid virtualization setup:

* **Host Machine:** Zorin OS 17.3 (Linux-based Security Workstation)
* **Hypervisor:** Oracle VM VirtualBox
* **Attack Node:** Kali Linux (Virtualized)
* **Network Strategy:** Utilizing isolated "Host-Only" adapters for safe internal testing.

---

##  Tool Audit & Inventory
I perform regular audits to verify that my core libraries are functional.

| Tool | Category | Current Version | Status |
| :--- | :--- | :--- | :--- |
| **Nmap** | Network Discovery | `7.98` | ✅ Verified |
| **Wireshark** | Packet Analysis | `4.6.2` | ✅ Verified |
| **Gobuster** | Web Recon | `3.8` | ✅ Verified |
| **Burp Suite** | Web Proxy | `2025.11.6` | ✅ Verified |

### 🛠️ Verification Methodology
For each tool, I execute a baseline check to confirm binary integrity:
1. **Version Check:** `[tool_name] --version` to ensure no outdated vulnerabilities exist in the tool itself.
2. **Functional Test:** Executing a "Ping Sweep" (Nmap) or "Directory Scan" (Gobuster) to confirm environmental variables are correctly mapped.

---

##  Proof of Functionality
### Activity: Network Recon Verification
I used **Nmap** within my Kali VM to verify connectivity to the local subnet.

**Command:** `nmap -sV 192.168.1.63`

---

##  Security Best Practices
* **Isolation:** Tools are never run directly on the host OS when testing external targets.
* **Ethics:** All scans are performed on networks I own or have explicit permission to audit.
* **Log Management:** Every scan is logged using `-oN` for future auditing and forensics.
