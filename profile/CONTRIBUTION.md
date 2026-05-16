# CONTRIBUTING.md
## Technical Contribution & Engineering Standards

Welcome to the TUINNOV8 SOLUTIONS LTD engineering ecosystem. This document defines the engineering workflows, continuous integration guidelines, and code quality benchmarks required for all internal engineering teams, startup accelerator founders, and external tech partners.

---

## 1. Code of Conduct & Commitments 🤝
As a software engineer or collaborator within TUINNOV8, you are expected to write secure, performant, and self-documenting code. Our primary focus is building resilient **E-Health systems, Automation workflows, and AI engines** that impact lives across Kenya and the broader East African market. Treat code safety and data privacy with utmost priority.

---

## 2. Git Workflow & Branching Strategy 🌿

We use a modified Git Flow model to ensure the stability of our core production environments.

### Branch Naming Conventions
Always branch from `develop` (or `main` depending on repository setup) using the following prefixes:
* `✨ feature/` — For new functionality or system modules (e.g., `feature/patient-triage-api`).
* `🐛 fix/` — For resolving bug tickets (e.g., `fix/postgres-connection-pool`).
* `🚑 hotfix/` — Immediate production patches branching directly from `main`.
* `🔨 refactor/` — Code performance optimizations or structural adjustments with no behavioral change.

### Commit Message Guidelines
We enforce semantic commit messages to automatically generate clean changelogs and track lifecycle upgrades. Commits must follow this format:
`type(scope): concise description in imperative mood`

**Examples:**
* `✨ feat(e-health): integrate automated SMS gateway alerts for medical appointments`
* `🐛 fix(automation): repair webhook failure recovery loop in n8n pipeline`
* `📝 docs(readme): update proprietary license references and contact info`

---

## 3. Code Review & Pull Request Protocol 🚀

1. **Before Submitting a Pull Request (PR):**
   * Sync your branch with the target branch upstream (`git pull origin develop`).
   * Execute localized test suites and verify all tests pass.
   * Run local linting tools to format the code properly.
2. **Opening the PR:**
   * Provide a concise description detailing what changes were made and why.
   * Reference any relevant internal task or issue tracking IDs.
3. **Review Lifecycle:**
   * Every PR requires at least **one approved review** from a Senior Systems Engineer or Tech Lead before merging.
   * Maintain zero breaking changes to existing database schemas unless accompanied by structured migration scripts.

---

## 4. Crucial Security Compliance (Zero-Leakage Policy) 🔒

Due to the sensitive nature of our E-Health data environments and proprietary business automations, strict security protocols must be followed:
* **No Secrets in Source:** Never hardcode API keys, encryption secrets, database passwords, or server gateway credentials.
* **Environment Configuration:** Use `.env.example` files to document needed keys. Real values must be injected at runtime using secure container environment variables or specialized secret managers.
* **Pre-Commit Hooks:** Ensure local repositories utilize secret-scanning tools (like `gitleaks` or `trufflehog`) to prevent accidentally staging confidential details.

---

## 5. Technology Stack Expectations 🛠️
When writing or reviewing code for our primary pillars, verify alignment with our standard technical baselines:
* **E-Health Backbone:** Highly documented APIs, strict adherence to medical data privacy standards, and efficient relational database modeling.
* **AI & Automation:** Clean payload mapping, error-catch blocks on all third-party API nodes, and optimized asynchronous processing.

Thank you for innovating with us. **Let us innovate! / Tuinnov8!** 🚀

---

## 📩 Contact & Support

For technical inquiries, security reports, or partnership discussions, reach out to our engineering leadership:

[![Website](https://img.shields.io/badge/Website-tuinnov8.com-blue?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.tuinnov8.com)
[![Email](https://img.shields.io/badge/Email-ngemuantony%40tuinnov8.com-red?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ngemuantony@tuinnov8.com)