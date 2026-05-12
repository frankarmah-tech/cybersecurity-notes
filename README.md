# 🔐 Cybersecurity Notes — Fundamentals, Tools & Best Practices

> A practical reference guide covering cybersecurity fundamentals, common threats, tools, and defence strategies — by **Frank Armah**, Cybersecurity Certified Professional (ZSecurity).

---

## 👋 About This Repository

This repo documents my cybersecurity knowledge and hands-on learning. It covers:

- ✅ Core cybersecurity concepts and terminology
- ✅ Common attack types and how they work
- ✅ Defence strategies and best practices
- ✅ Essential tools every IT professional should know
- ✅ Real-world security scenarios and how to handle them

---

## 📜 Certification

| Certificate | Issuer |
|---|---|
| 🔐 Cybersecurity Fundamentals | ZSecurity |

---

## 📚 Table of Contents

1. [Core Concepts](#core-concepts)
2. [Common Threats & Attacks](#common-threats--attacks)
3. [Defence Strategies](#defence-strategies)
4. [Essential Security Tools](#essential-security-tools)
5. [Network Security](#network-security)
6. [Cybersecurity in the Workplace](#cybersecurity-in-the-workplace)
7. [Real-World Scenarios](#real-world-scenarios)
8. [Security Checklist](#security-checklist)
9. [Resources](#resources)

---

## 🧠 Core Concepts

### The CIA Triad
The foundation of all cybersecurity:

| Principle | Meaning | Example |
|---|---|---|
| **Confidentiality** | Only authorised users can access data | Password protection, encryption |
| **Integrity** | Data is accurate and hasn't been tampered with | File hashing, digital signatures |
| **Availability** | Systems and data are accessible when needed | Backups, redundancy, uptime monitoring |

---

### Key Terminology

| Term | Definition |
|---|---|
| **Vulnerability** | A weakness in a system that can be exploited |
| **Exploit** | A method used to take advantage of a vulnerability |
| **Threat** | Any potential danger to a system or data |
| **Risk** | The likelihood and impact of a threat being realised |
| **Attack Surface** | All the points where an attacker could try to enter |
| **Zero-Day** | A vulnerability unknown to the software vendor |
| **Patch** | A software update that fixes a security vulnerability |
| **Authentication** | Verifying who a user is |
| **Authorisation** | Determining what a user is allowed to do |
| **Encryption** | Converting data into unreadable format without a key |

---

## ⚠️ Common Threats & Attacks

### 1. Phishing
**What it is:** Fraudulent emails or messages that trick users into revealing credentials or clicking malicious links.

**How to spot it:**
- Urgent or threatening language
- Suspicious sender email address
- Generic greetings ("Dear Customer")
- Links that don't match the claimed website
- Requests for passwords or personal info

**Defence:** Security awareness training, email filtering, multi-factor authentication (MFA)

---

### 2. Malware
**What it is:** Malicious software designed to damage, disrupt, or gain unauthorised access to systems.

**Types:**
| Type | Description |
|---|---|
| **Virus** | Attaches to files and spreads when opened |
| **Ransomware** | Encrypts files and demands payment |
| **Spyware** | Secretly monitors user activity |
| **Trojan** | Disguises itself as legitimate software |
| **Worm** | Self-replicates across networks without user action |

**Defence:** Antivirus software, regular updates, user education

---

### 3. Man-in-the-Middle (MitM) Attack
**What it is:** Attacker secretly intercepts communication between two parties.

**Common scenarios:**
- Public Wi-Fi interception
- ARP spoofing on local networks
- SSL stripping

**Defence:** Use HTTPS, VPNs, avoid public Wi-Fi for sensitive tasks

---

### 4. Denial of Service (DoS/DDoS)
**What it is:** Flooding a system with traffic to make it unavailable to legitimate users.

**Defence:** Firewalls, rate limiting, DDoS protection services, load balancing

---

### 5. SQL Injection
**What it is:** Inserting malicious SQL code into input fields to manipulate databases.

**Example:**
```sql
-- Normal input: username
-- Malicious input:
' OR '1'='1
```

**Defence:** Input validation, parameterised queries, web application firewalls (WAF)

---

### 6. Social Engineering
**What it is:** Manipulating people psychologically to reveal confidential information.

**Tactics:**
- Pretexting (creating a fake scenario)
- Baiting (leaving infected USB drives)
- Tailgating (following someone into a secure area)
- Vishing (voice phishing over phone calls)

**Defence:** Staff training, strict verification policies, security culture

---

### 7. Brute Force Attack
**What it is:** Systematically trying every possible password combination until the correct one is found.

**Defence:** Strong passwords, account lockout policies, MFA, CAPTCHA

---

## 🛡️ Defence Strategies

### Defence in Depth
Using multiple layers of security so that if one fails, others still protect the system.

```
Layer 1 → Physical Security (locked server rooms)
Layer 2 → Network Security (firewalls, IDS)
Layer 3 → Endpoint Security (antivirus, EDR)
Layer 4 → Application Security (input validation, WAF)
Layer 5 → Data Security (encryption, backups)
Layer 6 → User Security (MFA, training)
```

---

### Principle of Least Privilege
Users should only have access to what they need to do their job — nothing more.

✅ **Good:** IT support staff can reset passwords but cannot modify firewall rules
❌ **Bad:** Every employee has admin access to all systems

---

### Zero Trust Security Model
**"Never trust, always verify"** — assume every user and device could be compromised.

Key principles:
- Verify every user, every time
- Limit access to only what's needed
- Monitor and log all activity
- Assume breach has already occurred

---

## 🧰 Essential Security Tools

| Tool | Category | Use |
|---|---|---|
| **Nmap** | Network Scanner | Discover hosts and open ports on a network |
| **Wireshark** | Packet Analyser | Capture and analyse network traffic |
| **Metasploit** | Penetration Testing | Test systems for vulnerabilities |
| **Burp Suite** | Web Security | Test web application security |
| **John the Ripper** | Password Testing | Test password strength |
| **Nessus** | Vulnerability Scanner | Scan systems for known vulnerabilities |
| **Snort** | IDS/IPS | Detect and prevent network intrusions |
| **OpenVAS** | Vulnerability Scanner | Open-source vulnerability assessment |

---

## 🌐 Network Security

### Firewall Types
| Type | Description |
|---|---|
| **Packet Filtering** | Filters traffic based on IP, port, protocol |
| **Stateful Inspection** | Tracks connection state for better filtering |
| **Application Layer** | Inspects traffic at application level (Layer 7) |
| **Next-Gen Firewall (NGFW)** | Combines traditional firewall with IDS/IPS, DPI |

---

### Common Ports to Know

| Port | Protocol | Security Note |
|---|---|---|
| 22 | SSH | Secure — but restrict access |
| 23 | Telnet | ⚠️ Insecure — use SSH instead |
| 80 | HTTP | ⚠️ Unencrypted — use HTTPS |
| 443 | HTTPS | Secure web traffic |
| 3389 | RDP | ⚠️ Common attack target — restrict access |
| 21 | FTP | ⚠️ Insecure — use SFTP instead |

---

### VPN (Virtual Private Network)
Encrypts internet traffic and masks IP address.

**Use cases:**
- Secure remote work connections
- Protecting data on public Wi-Fi
- Accessing company resources remotely

---

## 🏢 Cybersecurity in the Workplace

### Security Awareness Training Topics
- How to identify phishing emails
- Password hygiene and management
- Safe use of USB devices
- Social engineering awareness
- Incident reporting procedures
- Safe internet browsing habits

### Incident Response Steps
```
1. IDENTIFY   → Detect and confirm the incident
2. CONTAIN    → Isolate affected systems immediately
3. ERADICATE  → Remove the threat completely
4. RECOVER    → Restore systems and data
5. LESSONS    → Document and improve defences
```

### Password Best Practices
- ✅ Minimum 12 characters
- ✅ Mix of uppercase, lowercase, numbers, symbols
- ✅ Different password for every account
- ✅ Use a password manager
- ✅ Enable Multi-Factor Authentication (MFA)
- ❌ Never share passwords
- ❌ Never use personal info (birthdays, names)
- ❌ Never reuse old passwords

---

## 🌍 Real-World Scenarios

### Scenario 1 — Phishing Attack at a Utility Company
**Situation:** An employee receives an email claiming to be from IT, asking them to reset their password urgently via a link.

**Red flags:**
- Urgent language
- Link goes to a non-company domain
- Email from external address

**Response:**
1. Do NOT click the link
2. Report to IT department immediately
3. IT investigates and blocks the sender
4. Send security awareness reminder to all staff

---

### Scenario 2 — Ransomware Infection
**Situation:** A staff member opens an email attachment and files start getting encrypted.

**Immediate response:**
1. Disconnect the device from the network immediately
2. Notify IT security team
3. Identify scope — which systems are affected
4. Restore from clean backups
5. Investigate how the attack entered
6. Patch the vulnerability

---

### Scenario 3 — Unauthorised Network Access
**Situation:** Security logs show login attempts from an unknown IP address at 3am.

**Response:**
1. Block the IP address at the firewall
2. Review all login logs for that period
3. Force password reset for targeted accounts
4. Enable MFA on all accounts
5. Investigate if any data was accessed

---

## ✅ Security Checklist

### For IT Professionals
- [ ] All systems patched and up to date
- [ ] Firewall rules reviewed and documented
- [ ] Unused ports and services disabled
- [ ] MFA enabled on all critical systems
- [ ] Backups tested and verified
- [ ] Access rights reviewed (least privilege)
- [ ] Security logs monitored regularly
- [ ] Staff security awareness training conducted
- [ ] Incident response plan documented and tested
- [ ] Antivirus/EDR deployed on all endpoints

---

## 📖 Resources

- [OWASP Top 10](https://owasp.org/www-project-top-ten/) — Top 10 web application security risks
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework) — Industry standard security framework
- [ZSecurity](https://zsecurity.org/) — My certification platform
- [Cybrary](https://www.cybrary.it/) — Free cybersecurity courses
- [TryHackMe](https://tryhackme.com/) — Hands-on cybersecurity labs
- [Have I Been Pwned](https://haveibeenpwned.com/) — Check if your email has been breached

---

## 🤝 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-frank--armah--tech-blue?logo=linkedin)](https://www.linkedin.com/in/frank-armah-tech)
[![GitHub](https://img.shields.io/badge/GitHub-frankarmah--tech-black?logo=github)](https://github.com/frankarmah-tech)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit%20Site-cyan?logo=google-chrome)](https://frankarmah-tech.github.io/frank-armah-portfolio)
[![Email](https://img.shields.io/badge/Email-frankarmah124@gmail.com-red?logo=gmail)](mailto:frankarmah124@gmail.com)

---

⭐ *If you find this useful, feel free to star the repo!*

*— Frank Armah | IT Professional | Ghana 🇬🇭*
