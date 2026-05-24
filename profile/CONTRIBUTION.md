<div align="center">

# 🤝 TUINNOV8 — Contribution Guidelines

**Technical Contribution & Engineering Standards**

_Welcome to the TUINNOV8 SOLUTIONS LTD engineering ecosystem._

[![Tech Team](https://img.shields.io/badge/Tech_Team-tech%40tuinnov8.com-8B5CF6?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tech@tuinnov8.com)
[![Website](https://img.shields.io/badge/Website-tuinnov8.com-6C63FF?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.tuinnov8.com)

</div>

---

This document defines the engineering workflows, CI/CD guidelines, and code quality benchmarks required for all internal engineering teams, startup accelerator founders, and external technology partners.

---

## 1. 🤝 Code of Conduct & Commitments

As a software engineer or collaborator within TUINNOV8, you are expected to write **secure, performant, and self-documenting code**. Our primary focus is building resilient **E-Health systems, Automation workflows, and AI engines** that impact lives across Kenya and the broader East African market.

> 🔒 Treat code safety and data privacy with utmost priority at all times.

---

## 2. 🌿 Git Workflow & Branching Strategy

We use a **modified Git Flow** model to ensure the stability of our core production environments.

### Branch Naming Conventions

Always branch from `develop` (or `main` depending on repository setup) using the following prefixes:

| Prefix | Purpose | Example |
|:------:|:--------|:--------|
| ✨ `feature/` | New functionality or system modules | `feature/patient-triage-api` |
| 🐛 `fix/` | Bug ticket resolutions | `fix/postgres-connection-pool` |
| 🚑 `hotfix/` | Immediate production patches from `main` | `hotfix/auth-token-critical` |
| 🔨 `refactor/` | Performance or structural improvements | `refactor/celery-task-routing` |

### Commit Message Guidelines

We enforce **semantic commit messages** to automatically generate clean changelogs:

```
type(scope): concise description in imperative mood
```

**Examples:**
- `✨ feat(e-health): integrate automated SMS gateway alerts for medical appointments`
- `🐛 fix(automation): repair webhook failure recovery loop in pipeline`
- `📝 docs(readme): update proprietary license references and contact info`

---

## 3. 🚀 Code Review & Pull Request Protocol

### Before Submitting a Pull Request (PR):
1. Sync your branch with the target branch upstream (`git pull origin develop`)
2. Execute localized test suites and verify **all tests pass**
3. Run local linting tools to format the code properly

### Opening the PR:
1. Provide a concise description detailing **what** changed and **why**
2. Reference any relevant internal task or issue tracking IDs
3. Ensure the PR targets the correct base branch

### Review Lifecycle:
- Every PR requires at least **one approved review** from a Senior Systems Engineer or Tech Lead
- Maintain **zero breaking changes** to existing database schemas unless accompanied by structured migration scripts
- CI/CD checks must pass before merge approval

---

## 4. 🔒 Security Compliance — Zero-Leakage Policy

Due to the sensitive nature of our E-Health data environments and proprietary business automations, strict security protocols must be followed:

| Requirement | Details |
|:------------|:--------|
| **No Secrets in Source** | Never hardcode API keys, encryption secrets, database passwords, or gateway credentials |
| **Environment Config** | Use `.env.example` files to document needed keys. Real values injected at runtime via secure container variables |
| **Pre-Commit Hooks** | Ensure local repos utilize secret-scanning tools (`gitleaks` or `trufflehog`) |
| **OWASP Compliance** | All code must be reviewed against the latest **OWASP Top 10** checklist |

---

## 5. 🛠️ Technology Stack Alignment

When writing or reviewing code, verify alignment with our standard technical baselines:

<div align="center">

| Layer | Technologies |
|:------|:------------|
| **Backend** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white) |
| **Frontend** | ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) |
| **Databases** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **Async** | ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white) ![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white) |
| **Communication** | ![Discord](https://img.shields.io/badge/Discord-5865F2?style=flat-square&logo=discord&logoColor=white) |

</div>

---

## 6. 🏗️ Three-Tier Contribution Model

Contributions are structured across three tiers to ensure quality, security, and progressive trust:

<table>
<tr>
<td align="center" width="33%">

### 🥉 Tier 1 — Community

- Bug reports & feature requests
- Documentation improvements
- Small UI/UX fixes
- Issue triage & discussions
- **No code merge access**

</td>
<td align="center" width="33%">

### 🥈 Tier 2 — Contributor

- Code contributions via PR
- Test coverage improvements
- Code review participation
- Architecture proposals
- **PR-based merge access**

</td>
<td align="center" width="33%">

### 🥇 Tier 3 — Core

- Direct commit access
- Release management
- Security-critical changes
- Infrastructure & DevOps
- **Full repository access**

</td>
</tr>
</table>

> 🌱 **Advancement:** Contributors advance through tiers based on consistency, quality, and alignment with TUINNOV8 engineering values.

---

## 7. 📋 PR Checklist

Before submitting your pull request, ensure you've completed:

- [ ] Code compiles and runs without errors
- [ ] All existing and new tests pass
- [ ] Linting and formatting checks pass
- [ ] No secrets, credentials, or API keys committed
- [ ] Semantic commit messages used
- [ ] PR description clearly explains changes
- [ ] Relevant issue/task IDs referenced
- [ ] Database migrations included (if schema changed)
- [ ] Documentation updated (if API changed)

---

<div align="center">

_Thank you for innovating with us._

### **Let us innovate! / Tuinnov8!** 🚀

---

## 📩 Contact & Support

For technical inquiries, security reports, or partnership discussions:

[![Tech Team](https://img.shields.io/badge/Tech_Team-tech%40tuinnov8.com-8B5CF6?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tech@tuinnov8.com)
[![Website](https://img.shields.io/badge/Website-tuinnov8.com-6C63FF?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.tuinnov8.com)

<br/>

<sub>

**TUINNOV8 SOLUTIONS LTD** · Nairobi, Kenya 🇰🇪

© 2026 TUINNOV8 SOLUTIONS LTD. All rights reserved.

</sub>

</div>