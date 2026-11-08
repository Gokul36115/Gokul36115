# Hello, I'm Gokul 👋

**Middleware Engineer @ Kyndryl** · AWS · DevOps · SRE

🌐 **Portfolio:** [gokul36115.github.io](https://gokul36115.github.io)

I keep business-critical Java platforms running in production. For **3.2+ years** I've worked on a **3,000+ server estate** across **Linux, AIX and Windows**, running **IBM WebSphere ND, Liberty and IBM HTTP Server**, on **24×7 rotational on-call** with **production releases every weekend**.

I apply the same reliability mindset to cloud and Kubernetes: systems that **detect failures, recover automatically and alert the right people**, built with **Terraform, Docker, Kubernetes, Argo CD (GitOps), Prometheus, Grafana and AWS serverless**, and secured with **SSO (OIDC)**.

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
- Migrate applications to **Okta SSO**: configure the Okta client ID and secret on WebSphere, Liberty and IHS so apps authenticate through single sign-on
- Run **quarterly fix pack upgrades** for WebSphere, IHS, Liberty and plug-ins across the estate

**Day to day**
- Production application deployments, JVM restarts and health checks
- Troubleshooting JVM, IHS and plug-in issues through logs and thread/heap dumps
- SSL/TLS certificate renewals, keystore management and CVE remediation

---

## 🚀 Featured Projects

Three projects, one theme: **failures should be detected, healed and alerted on automatically.** First on a single cloud server, then at Kubernetes platform level, then serverless with no servers to manage at all.

### 1️⃣ [Self-Healing Containerized Java Application on AWS](https://github.com/Gokul36115/self-healing-java-app-aws)
A Spring Boot service on EC2 that recovers from crashes and OutOfMemoryErrors and e-mails an alert within about a minute.

- 🔍 **Found a silent failure:** after an `OutOfMemoryError` the JVM kept returning 500s while Docker still reported it `healthy`. Fixed with `-XX:+ExitOnOutOfMemoryError`, so the JVM exits and Docker restarts it.
- 🏗️ **Terraform:** 19 AWS resources (VPC, IAM, EC2 with IMDSv2, CloudWatch, SNS), no SSH, applied from a reviewed plan
- 🔁 **Jenkins CI/CD:** build → test → Docker image → smoke test → push → deploy with health check
- 🚨 **Monitoring:** CloudWatch log metric → alarm → SNS e-mail, verified live

`Java` `Spring Boot` `Docker` `Jenkins` `Terraform` `AWS EC2 · VPC · IAM` `CloudWatch` `SNS`

### 2️⃣ [Self-Healing Kubernetes Platform: GitOps · SLOs · Observability](https://github.com/Gokul36115/k8s-selfheal-platform)
The same service on Kubernetes, where the cluster heals the app, Git is the source of truth, and reliability is measured with SLOs.

- ☸️ **Kubernetes self-healing:** startup/liveness/readiness probes, zero-downtime rolling updates, PodDisruptionBudget, HPA autoscaling 2 → 5 pods
- 🔄 **GitOps with Argo CD:** auto-sync and drift correction; CI is read-only on the repo and releases are a reviewed Git commit
- 📈 **SRE observability:** Prometheus + Grafana, a 99.5% availability SLO with multi-window error-budget burn-rate alerts
- 💥 **Chaos-tested live:** 4 automatic container restarts, alerts fired, pods recovered with zero manual steps
- 🛠️ **Real troubleshooting:** Grafana `CrashLoopBackOff` → `OOMKilled` → fixed through a Git commit

`Kubernetes (k3s)` `Helm` `Argo CD` `GitHub Actions` `Prometheus` `Grafana` `Alertmanager` `Docker`

### 3️⃣ [Site Watchdog: Serverless Uptime & TLS Monitor with SSO Dashboard](https://github.com/Gokul36115/site-watchdog-serverless)
A serverless monitor that checks websites every 15 minutes for uptime, response time and certificate expiry, alerts on Telegram, and serves a live dashboard behind single sign-on. **[Live dashboard ↗](https://gokul36115.github.io/site-watchdog-serverless/)** (login required)

- ⏱️ **Serverless checks:** EventBridge runs a Python Lambda every 15 minutes: HTTP status, response time and days until the SSL/TLS certificate expires
- 🚨 **One alert, all problems:** a single Telegram message lists every failing site; verified with an expired certificate and a DNS failure
- 🔐 **SSO with Auth0 (Okta):** OIDC login with PKCE; API Gateway's JWT authorizer rejects requests without a valid token (`401`) before the Lambda runs
- 🛡️ **Secure by design:** bot token in SSM Parameter Store (`SecureString`, kept out of Terraform state), least-privilege IAM, CORS locked to the dashboard, API throttling
- 🏗️ **Terraform:** 13 AWS resources, running cost close to ₹0

`Python` `AWS Lambda` `API Gateway` `EventBridge` `SSM Parameter Store` `Auth0 (Okta)` `OIDC · JWT` `Terraform` `CloudWatch`

---

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| **Middleware** | IBM WebSphere ND, Liberty, IBM HTTP Server, web server plug-ins, JVM tuning, KDB keystores, SSL/TLS, Okta SSO |
| **CI/CD & GitOps** | IBM UrbanCode Deploy (UCD), Jenkins, GitHub Actions, Argo CD |
| **Infrastructure as Code & Scripting** | Terraform, Helm, Bash, Python |
| **Cloud** | AWS (EC2, VPC, IAM, S3, CloudWatch, SNS, Lambda, API Gateway, EventBridge, SSM Parameter Store), Microsoft Azure |
| **Identity & Security** | Okta SSO, Auth0, OIDC, JWT, PKCE, IAM least privilege, secrets management |
| **Containers & Kubernetes** | Docker, Kubernetes (k3s), Helm, HPA, probes, PodDisruptionBudgets |
| **Observability & SRE** | Prometheus, Grafana, Alertmanager, CloudWatch, SLOs and error budgets |
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

- 🔐 Kubernetes Ingress with automatic TLS (cert-manager), and SSO (OIDC) for Grafana and Argo CD
- ☁️ AWS architecture: Solutions Architect track, and running these platforms on EKS
- ⚙️ Platform engineering: GitOps, policy as code and reliability at scale

---

## 📬 Let's Connect

- 🌐 [Portfolio](https://gokul36115.github.io)
- 💼 [LinkedIn](https://www.linkedin.com/in/gokul36115)
- ✉️ gokul36115@gmail.com
- 📍 Chennai, India
