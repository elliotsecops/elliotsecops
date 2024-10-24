# Gabriel Palacios — Elliot

**Security Architect · Cloud · DevSecOps · Web3**

I design and secure infrastructure that moves money: cloud boundaries, CI/CD,
authorization paths, key custody, and protocol accounting. For fintech and
on-chain systems where a mistake is a loss, not a ticket.

**31+ vulnerabilities found and fixed in a production financial system before
users touched it.** One paid critical on Immunefi.

📫 elliotsecops@protonmail.com  
🐦 [@elliotsecops](https://x.com/elliotsecops) — 5.3k engineers, founders and security folks  
🔓 **Reviews open — Q4 2026**

---

## What I'm Working On

I build and operate payment infrastructure across EVM and non-EVM chains, and
tooling for vulnerability intake, triage and responsible disclosure. The
systems are private. The output isn't: the findings below, the tools in this
profile, and the writeups I publish.

That constraint is the job. Most of what I know about securing money systems
came from operating them, not from auditing someone else's.

---

## Findings

| Category | What I Found | What I Built |
|----------|--------------|--------------|
| **Authentication** | JWT token/algorithm confusion attacks | Hardened token validation with explicit algorithm enforcement and key rotation |
| **Authorization** | IDOR vulnerabilities in financial endpoints | Resource-level access controls with user-scoped validation on every balance operation |
| **Key Management** | Weak key derivation, no rotation strategy | HD wallet architecture with zero-trust key rotation and hardware custody integration |
| **Deposit Attribution** | Race conditions that could credit treasury funds to the wrong user | Database-level guards with atomic balance updates and deposit reconciliation locks |
| **Financial Integrity** | Balance drift with no audit trail | Double-entry journaling with forensic reconciliation and automated correction |
| **Operational Security** | Silent failures in critical paths | Fail-closed architecture: no observability, no operation. Telemetry, alerting and circuit breakers on every critical flow |

> *"Fail-closed. If I can't see it, it doesn't run. If I can't verify it, it doesn't ship."*

This isn't theoretical. I've done incident response on live financial systems —
forensic deposit reconciliation, balance correction with double-entry
journaling, and root-cause analysis with real user funds at risk.

---

## Beyond Financial Infrastructure

I research vulnerabilities across DeFi, staking, vaults, lending and protocol
accounting systems, in Solidity and Rust across EVM, Solana and Substrate
ecosystems. What I look for:

* Protocol accounting and state desynchronization
* Vault inflation and share-price manipulation
* Liquidation and margin edge cases
* Oracle and pricing assumptions
* Staking and validator reward mechanisms
* Access-control failures and privilege boundaries
* Token issuance and redemption logic
* Economic exploits and fund-loss scenarios
* Cross-contract and integration risk

My research has involved protocol reviews and disclosures across Ethereum,
Arbitrum, Solana, BNB Chain and Polkadot ecosystems — lending markets, liquid
staking, vault architectures, yield infrastructure, validator systems and
accounting layers.

---

## What I Do For Other Teams

Building financial infrastructure and analyzing production protocols taught me
something most security consultants don't understand: **security that slows
down shipping is security that gets bypassed.**

I work with teams building systems where security failures have real
consequences — financial infrastructure, Web3 protocols, cloud-native
applications, platforms handling sensitive data.

I don't deliver PDF audits that sit in a drawer. I help teams identify
architectural risks and implement controls that survive contact with production.

**I help with:**

* **Cloud Security & Architecture:** AWS/GCP hardening, IAM design, network segmentation, infrastructure reviews, operational resilience
* **DevSecOps & Platform Engineering:** Secure CI/CD, container and Kubernetes security, secrets management, deployment workflows
* **Application Security:** Authentication, authorization, API security, dependency risk, threat modeling, secure system design
* **Web3 Security:** Protocol reviews, smart contract risk, protocol accounting, staking, vaults, lending markets, disclosure workflows
* **Key Management & Signing:** HD wallet architecture, key rotation, custody integration, transaction authorization paths

**The difference:** I've been the person accountable for protecting real funds —
handling incident response and making security decisions under operational
pressure. I understand both the engineering reality and the requirements of
systems that cannot afford to fail.

---

## Certifications & Credentials

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

**Currently pursuing:** GCP Security — Specialty

---

## Featured Projects

Tools I build, use in production, and maintain in the open.

### [API-Security-Scanner](https://github.com/elliotsecops/API-Security-Scanner)
**Go · React · Docker · Prometheus**

Automated API security testing platform with a web GUI. Built after finding
auth bypass and injection flaws in payment endpoints during an internal review.

- SQL/NoSQL injection, XSS, auth bypass and parameter tampering detection
- OpenAPI/Swagger import for generated test targets
- Multi-format reporting (JSON, HTML, CSV) with risk scoring
- React dashboard for real-time monitoring and historical comparison

---

### [Docker-Security-Scanner](https://github.com/elliotsecops/Docker-Security-Scanner)
**Go**

Lightweight container security scanner for CI/CD. I gate deployments with it
before images reach production.

- Root user detection, exposed ports, missing resource limits
- Hardcoded secrets scanning in container environment variables
- Image integrity validation
- Structured JSON output for pipeline automation

---

### [Secure-Fortress-Linux](https://github.com/elliotsecops/Secure-Fortress-Linux)
**Ansible · Bash · Wazuh**

Linux hardening framework. The baseline I deploy on every server that touches
money.

- Automated updates, UFW firewall, SSH hardening (no root, key-only)
- Password policy enforcement (12+ chars, 4 character classes)
- Wazuh SIEM agent for file integrity monitoring and rootkit detection
- CIS Benchmark-aligned configuration
- Single-server (Bash) or fleet-wide (Ansible) deployment

---

### [Ghost-Tunnel](https://github.com/elliotsecops/Ghost-Tunnel)
**Python · Tor · SSH · SOCKS**

Anonymous SSH tunneling through Tor with multi-hop proxies. Used for secure
operational access in restricted environments and red-team exercises.

---

### [Portseeker_Go](https://github.com/elliotsecops/Portseeker_Go)
**Go · Nmap · CVE Databases**

Fast port scanner with CVE matching. First tool I run on any new
infrastructure before it joins the network.

---

### [GoKubeDeploy](https://github.com/elliotsecops/GoKubeDeploy)
**Go · Kubernetes · GitHub Actions · JWT**

Reference architecture for secure Go deployments on Kubernetes.

- JWT auth, NetworkPolicies, Kubernetes secrets handling
- Liveness/readiness probes for zero-downtime deployments
- GitHub Actions CI/CD with Trivy scanning
- Fluent Bit centralized logging

---

## Additional Tools

- [**Packet-Capture**](https://github.com/elliotsecops/Packet-Capture) — Forensic `.pcap` analysis with pyshark for post-incident investigation
- [**Network-Traffic-Anomaly-Detector**](https://github.com/elliotsecops/Network-Traffic-Anomaly-Detector) — Real-time capture with ML-based anomaly detection (IsolationForest)
- [**Network-Auditor**](https://github.com/elliotsecops/Network-Auditor) — Linux network configuration audit and reporting
- [**IoTSecurityTool**](https://github.com/elliotsecops/IoTSecurityTool) — Nmap-based IoT discovery and NSE vulnerability scanning

---

## How I Work

**I ship under constraints.** I've built systems that have to be secure by
default, observable by design, and recoverable without a human at 3 AM.

**I build, then I document.** Every project ships with deployment instructions,
configuration examples and honest limitations. No "enterprise-grade" buzzwords
for a focused utility.

**Security that blocks shipping gets bypassed.** I know the pressure of product
deadlines and live users. I find the fixes that protect the business without
grinding development to a halt.

---

## Content & Community

I write about security, fintech infrastructure and what it actually takes to
build safe money systems — for engineers, founders and fintech operators.

**Topics:**

- Practical cloud hardening for teams without a security team
- Key custody, signing policy and treasury operations
- Deposit reconciliation and financial integrity
- Open-source security tooling and real production use
- Fintech compliance: what you need vs. what auditors want
- DevSecOps pipelines that don't slow down developers

Follow on [X](https://x.com/elliotsecops).

---

## Tech Stack

**Cloud:** AWS · Google Cloud Platform · Cloudflare

**Blockchain & Web3:** EVM · Solana · DeFi Protocols · Smart Contract Security · Protocol Accounting · Transaction Processing · Key Management · Reconciliation

**Smart Contract Languages:** Solidity · Rust

**Containers & Orchestration:** Docker · Kubernetes · Helm

**Infrastructure as Code:** Terraform · Ansible

**Languages:** Go · Python · Bash · HCL

**Security Research:** Web3 Vulnerability Research · Protocol Reviews · Vulnerability Disclosure · Threat Modeling · DeFi Risk Analysis

**Security & Monitoring:** Wazuh · Nmap · Metasploit · Wireshark · Burp Suite · Trivy

**CI/CD & Automation:** GitHub Actions · GitLab CI

**Data & ML (Security Context):** scikit-learn · pandas · scapy

---

## Let's Work Together

I work with teams building products where security failures have real
consequences: financial infrastructure, Web3 protocols, cloud-native platforms,
systems handling sensitive data or critical operations.

**I can help you:**

* Design and harden cloud infrastructure before scale becomes a security problem
* Build secure CI/CD pipelines and deployment workflows
* Review application and protocol security assumptions before they become incidents
* Audit authorization and signing paths — who can move money, and who signs for it
* Improve observability, monitoring and incident response
* Establish practical controls without slowing product development

**Engagements:** fixed-scope reviews (typically two weeks), or monthly retainer.
Findings by severity with reproduction, a remediation patch, and a walkthrough
with your engineers. Fixed fee, quoted within 24 hours.

**Reviews open — Q4 2026.** One slot.

**📫 elliotsecops@protonmail.com**  
**🐦 [DM on X](https://x.com/elliotsecops)**
