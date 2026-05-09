# Gabriel Palacios - Alias: Elliot

**Security Engineer · Fintech Founder · DevSecOps · Ethical Hacking**

I build secure financial infrastructure for LATAM. Currently solo-founding a neobank handling real funds across 7 blockchains (EVM, Solana, and Stellar) while helping other early-stage startups harden their systems before they become headlines.

📫 elliotsecops@protonmail.com  
🐦 [Twitter](https://twitter.com/elliotsecops) — 5,200+ engineers, founders, and security folks

---

## Currently Building: LATAM Neobank

I'm the solo technical founder of a neobank operating across Latin America, processing real funds on 7 different blockchains. This isn't a side project. It's production financial infrastructure where a single bug means real money disappears.

**What that means in practice:**

- **Real funds, real risk.** Every line of code I write handles deposits, withdrawals, and balance movements that affect actual users.
- **7 blockchain integrations.** Each with its own key management model, transaction finality guarantees, and reconciliation logic.
- **Zero room for "good enough" security.** When you're the only technical person and the treasury is live, security isn't a checklist. It's survival.

**Security vulnerabilities I've identified and remediated (31+ to date):**

| Category | What I Found | What I Built |
|----------|--------------|--------------|
| **Authentication** | JWT token/algorithm confusion attacks | Hardened token validation with explicit algorithm enforcement and key rotation |
| **Authorization** | IDOR vulnerabilities in financial endpoints | Resource-level access controls with user-scoped validation on every balance operation |
| **Cryptographic Key Management** | Weak key derivation, lack of rotation strategy | HD wallet architecture with zero-trust key rotation and hardware wallet custody integration |
| **Deposit Attribution** | Race conditions that could credit treasury funds to wrong users | Database-level guards with atomic balance updates and deposit reconciliation locks |
| **Financial Integrity** | Potential for balance drift without audit trail | Double-entry journaling system with forensic reconciliation and automated balance correction |
| **Operational Security** | Silent failures in critical paths | Fail-closed architecture: no observability means no operation. Every critical flow has telemetry, alerting, and circuit breakers |

**Security philosophy from the trenches:**

&gt; *"Fail-closed. If I can't see it, it doesn't run. If I can't verify it, it doesn't ship."*

This isn't theoretical. I've done incident response on live financial systems — forensic deposit reconciliation, balance correction with double-entry journaling, and root-cause analysis under the pressure of real user funds at risk.

---

## What I Do For Other Startups

Building my own fintech taught me something most security consultants don't understand: **security that slows down shipping is security that gets bypassed.**

I operate as a **fractional security engineer** for startups with fresh funding and no security team. I don't deliver PDF audits that sit in a drawer. I write the Terraform, the Ansible playbooks, the Go tools, and the CI/CD pipelines that actually fix the gaps.

**I help with:**

- **Cloud Security Posture:** Hardening AWS and GCP environments, IAM lockdown, network policies, SOC 2 prep
- **Container & Kubernetes Security:** Image scanning, runtime policies, secrets management, RBAC, zero-downtime secure deployments
- **Application Security:** API vulnerability assessment, auth review, secure CI/CD design, dependency scanning
- **Linux Hardening & Monitoring:** Automated server hardening with Ansible, Wazuh SIEM, file integrity monitoring
- **Network Security:** Traffic analysis, anomaly detection, reconnaissance tooling, secure tunneling

**The difference:** I've been the founder who gets the 3 AM alert because a deposit didn't reconcile. I know which security fixes unblock enterprise deals and which ones are theater.

---

## Certifications & Credentials

Formal training that backs the hands-on work:

| Certification | Issuer | Date | What It Covers |
|---------------|--------|------|----------------|
| **Google Cloud Computing Foundations Certificate** | Google Cloud | Apr 2024 | Core GCP infrastructure, IAM, networking, security fundamentals |
| **Build a Secure Google Cloud Network** | Google Cloud | Apr 2024 | VPC design, firewall rules, load balancing, secure network architecture |
| **Ethical Hacker** | Cisco Networking Academy | Jan 2024 | Penetration testing methodology, vulnerability exploitation, defensive countermeasures |
| **Junior Cybersecurity Analyst Career Path** | Cisco | May 2023 | SOC operations, threat intelligence, incident response, security monitoring |
| **Network Defense** | Cisco | Apr 2023 | Perimeter security, intrusion detection/prevention, firewall architecture |
| **Cyber Threat Management** | Cisco | May 2023 | Threat landscape analysis, vulnerability management, risk assessment |
| **Network Support and Security** | Cisco | May 2023 | Enterprise network troubleshooting with integrated security controls |

*[View all verified badges on Credly](https://www.credly.com/users/gabriel-palacios.d1f87889)*

**Currently pursuing:** GCP Security - Specialty

---

## Featured Projects

Tools I build, use in my fintech, and maintain in the open.

### [API-Security-Scanner](https://github.com/elliotsecops/API-Security-Scanner)
**Go · React · Docker · Prometheus**

Automated API security testing platform with web GUI. Built after finding auth bypass and injection vulnerabilities in my own fintech's endpoints during internal review.

- SQL/NoSQL injection, XSS, auth bypass, and parameter tampering detection
- OpenAPI/Swagger spec import for auto-generated test targets
- Multi-format reporting (JSON, HTML, CSV) with risk scoring
- React dashboard for real-time monitoring and historical comparison

---

### [Docker-Security-Scanner](https://github.com/elliotsecops/Docker-Security-Scanner)
**Go**

Lightweight container security scanner for CI/CD pipelines. I use this to gate deployments in my own infrastructure before images hit production.

- Root user detection, exposed ports, missing resource limits
- Hardcoded secrets scanning in container environment variables
- Image integrity validation
- Structured JSON output for pipeline automation

---

### [Secure-Fortress-Linux](https://github.com/elliotsecops/Secure-Fortress-Linux)
**Ansible · Bash · Wazuh**

Linux hardening framework. The baseline I deploy on every server that touches my fintech's infrastructure.

- Automated updates, UFW firewall, SSH hardening (no root, key-only)
- Password policy enforcement (12+ chars, 4 character classes)
- Wazuh SIEM agent for file integrity monitoring and rootkit detection
- CIS Benchmark-aligned configurations
- Single-server (Bash) or fleet-wide (Ansible) deployment

---

### [Ghost-Tunnel](https://github.com/elliotsecops/Ghost-Tunnel)
**Python · Tor · SSH · SOCKS**

Anonymous SSH tunneling through Tor with multi-hop proxies. Used for secure operational access in restrictive environments and red-team exercises.

---

### [Portseeker_Go](https://github.com/elliotsecops/Portseeker_Go)
**Go · Nmap · CVE Databases**

Fast port scanner with CVE matching. First tool I run on any new infrastructure before it joins my network.

---

### [GoKubeDeploy](https://github.com/elliotsecops/GoKubeDeploy)
**Go · Kubernetes · GitHub Actions · JWT**

Production-ready template for secure Go deployments on Kubernetes. Reference architecture for my own microservices.

- JWT auth, NetworkPolicies, Kubernetes Secrets management
- Liveness/readiness probes for zero-downtime deployments
- GitHub Actions CI/CD with Trivy vulnerability scanning
- Fluent Bit centralized logging

---

## Additional Tools

- [**Packet-Capture**](https://github.com/elliotsecops/Packet-Capture) — Forensic `.pcap` analysis with pyshark for post-incident investigation
- [**Network-Traffic-Anomaly-Detector**](https://github.com/elliotsecops/Network-Traffic-Anomaly-Detector) — Real-time traffic capture with ML-based anomaly detection (IsolationForest)
- [**Network-Auditor**](https://github.com/elliotsecops/Network-Auditor) — Linux network configuration audit and reporting
- [**IoTSecurityTool**](https://github.com/elliotsecops/IoTSecurityTool) — Nmap-based IoT device discovery and NSE vulnerability scanning

---

## How I Work

**I ship under constraints.** As a solo founder, I don't have a security team to review my code. I have to build systems that are secure by default, observable by design, and recoverable without human intervention at 3 AM.

**I build, then I document.** Every project includes deployment instructions, configuration examples, and honest limitations. No "enterprise-grade" buzzwords when the tool is a focused utility.

**Security that blocks shipping gets bypassed.** I know the pressure of product deadlines and live users. I find the fixes that protect the business without grinding development to a halt.

---

## Content & Community

I write about security, fintech infrastructure, and the reality of building safe financial systems in LATAM. My audience is engineers, startup founders, and fintech operators — mostly across Latin America.

**Topics I cover:**
- Practical cloud hardening for startups without a security team
- Blockchain security: key management, deposit reconciliation, and treasury operations
- Open-source security tools and production usage
- Fintech compliance: what you actually need vs. what auditors want
- DevSecOps pipelines that don't slow down developers

Follow on [Twitter](https://twitter.com/elliotsecops).

---

## Tech Stack

**Cloud:** AWS · Google Cloud Platform  
**Blockchain:** 7 chains (EVM, Solana, and Stellar) - key management, transaction processing, reconciliation  
**Containers & Orchestration:** Docker · Kubernetes · Helm  
**Infrastructure as Code:** Terraform · Ansible  
**Languages:** Go · Python · Bash · HCL  
**Security & Monitoring:** Wazuh · Nmap · Metasploit · Wireshark · Burp Suite · Trivy  
**CI/CD & Automation:** GitHub Actions · GitLab CI  
**Data & ML (Security Context):** scikit-learn · pandas · scapy

---

## Let's Work Together

**If you're a startup founder with fresh funding and no security team, I can help you:**

- Pass your first enterprise **security questionnaire** without making things up
- Harden your cloud infrastructure before you scale
- Set up monitoring and incident response that actually works
- Build secure CI/CD pipelines that catch vulnerabilities before production

**If you're a fintech specifically:** I've lived the exact problems you're about to face. Deposit reconciliation, key custody, balance integrity, and the terror of your first production incident. I can help you avoid the mistakes I had to learn the hard way.

I work on a project basis or monthly retainer. No long-term contracts required.

**📫 elliotsecops@protonmail.com**  
**🐦 [DM me on Twitter](https://twitter.com/elliotsecops)**
