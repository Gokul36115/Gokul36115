# Hi, I'm Gokul 👋

**Middleware Engineer @ Kyndryl** · AWS · DevOps · SRE

I keep business-critical Java platforms running in production. For **3.2+ years** I've worked on a **3,000+ server estate** across **Linux, AIX and Windows**, running **IBM WebSphere ND, Liberty and IBM HTTP Server**, on **24×7 rotational on-call** with **production releases every weekend**.

I apply the same reliability mindset on AWS: systems that **detect failures, recover automatically and alert the right people**, built with **Terraform, Docker, Jenkins and CloudWatch**.

---

## 🏢 What I Do

**Production operations**
- 24×7 rotational on-call support for enterprise production environments
- Weekend change windows: production application releases and changes
- Incident response, root cause analysis and SOPs, following ITIL v4

**Middleware engineering**
- Build **IBM WebSphere ND** environments from scratch: cells, profiles, clusters, **IBM HTTP Server** and **web server plug-ins**
- Administer **IBM Liberty** servers alongside traditional WebSphere
- Configure **IBM UrbanCode Deploy (UCD)** for automated application deployments
- Run **quarterly fix pack upgrades** for WebSphere, IHS, Liberty and plug-ins across the estate

**Day to day**
- Production application deployments, JVM restarts and health checks
- Troubleshooting JVM, IHS and plug-in issues through logs and thread/heap dumps
- SSL/TLS certificate renewals, keystore management and CVE remediation

---

## 🚀 Featured Project

### 🩺 [Self-Healing Containerized Java Application on AWS](https://github.com/Gokul36115/self-healing-java-app-aws)
JVM crashes and OutOfMemoryErrors are problems I deal with in production. This project detects, recovers from and alerts on them automatically.

- 🔍 **Found a silent failure:** after an `OutOfMemoryError` the JVM kept returning 500s while Docker still reported it `healthy`. Fixed with `-XX:+ExitOnOutOfMemoryError`, so the JVM exits and Docker restarts it.
- 🏗️ **Terraform:** 19 AWS resources (VPC, IAM, EC2 with IMDSv2, CloudWatch, SNS), no SSH, applied from a reviewed plan
- 🔁 **Jenkins CI/CD:** build → test → Docker image → smoke test → push → deploy with health check
- 🚨 **Monitoring:** CloudWatch log metric → alarm → SNS e-mail, verified live in about 1 minute

`Java` `Spring Boot` `Docker` `Jenkins` `Terraform` `AWS` `CloudWatch` `SNS`

---

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| **Middleware** | IBM WebSphere ND, Liberty, IBM HTTP Server, web server plug-ins, JVM tuning, KDB keystores, SSL/TLS |
| **Deployment & Automation** | IBM UrbanCode Deploy (UCD), Jenkins, Terraform, Bash |
| **Cloud** | AWS (EC2, VPC, IAM, S3, CloudWatch, SNS), Microsoft Azure |
| **Containers** | Docker, Docker Hub, Kubernetes |
| **Operating Systems** | Linux (RHEL, Ubuntu, Amazon Linux), AIX, Windows Server |
| **Operations** | 24×7 on-call, ITIL v4, incident and change management, RCA, SOPs |

---

## 🎓 Certifications

| Certification | Issued | Verify |
|---|---|---|
| **AWS Certified Cloud Practitioner** | Aug 2026 | [Credly badge](https://www.credly.com/badges/4b978eff-930c-437b-9c06-1a9a5053c8db) |
| **Microsoft Certified: Azure Administrator Associate (AZ-104)** | Apr 2026 | [Microsoft Learn](https://learn.microsoft.com/en-us/users/gokuln-7717/credentials/bf03700fb403d18c) |
| **Microsoft Certified: Security, Compliance, and Identity Fundamentals (SC-900)** | Jan 2025 | [Microsoft Learn](https://learn.microsoft.com/en-us/users/gokuln-7717/credentials/28cae4550809a0ec) |
| **Microsoft Certified: Azure Fundamentals (AZ-900)** | Dec 2023 | [Microsoft Learn](https://learn.microsoft.com/en-us/users/gokuln-7717/credentials/971b2d910f602c9f) |

---

## 🎯 Focus Areas

- ☸️ Kubernetes: deployments, health probes and scaling
- ☁️ AWS architecture: Solutions Architect track
- ⚙️ Infrastructure as code and CI/CD automation at scale

---

## 📬 Let's Connect

- 💼 [LinkedIn](https://www.linkedin.com/in/gokul36115)
- ✉️ gokul36115@gmail.com
- 📍 Chennai, India
