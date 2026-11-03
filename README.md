<div align="center">

# 🌌 Nexus

**The Ultimate Identity Hub for the Modern Web.**

*Welcome to this Galaxy full of infinite possibilities.*

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Status: Public Beta](https://img.shields.io/badge/Status-Public_Beta-orange.svg)](#)
[![Serverless](https://img.shields.io/badge/Serverless-Cloudflare_Workers-F38020?logo=cloudflare)](https://workers.cloudflare.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![JavaScript](https://img.shields.io/badge/JavaScript-100%25-yellow?logo=javascript)](https://github.com/CrCLARE/Nexus)

[Website](https://nexus.crclare.top) • [Documentation(Not yet completed)](https://sso.crclare.top) • [Report Bug](../../issues) • [Request Feature](../../issues)

</div>

---

## 🚀 What is Nexus?

**Nexus** is a lightweight, 100% pure JavaScript, open-source Single Sign-On (SSO) platform developed by **CrCLARE Studio**. 

Designed for zero-server-cost and extreme performance, Nexus injects enterprise-grade Zero Trust security into your ecosystem. Whether you are building a SaaS, a private forum, or just want to give your [Twikoo](https://twikoo.js.org) blog commenters a verified badge, Nexus is your ultimate identity foundation.

> ⚠️ **Note:** Nexus is currently in **Public Beta**. We are actively fixing edge cases and polishing the UI. Please use GitHub Issues for feedback!

---

## ✨ Why Nexus?

Break free from vendor lock-in and redefine your digital identity baseline.

- 🛡️ **Zero Trust Security:** Full support for WebAuthn/Passkey (e.g., YubiKey, iCloud Passkey) for physical-level anti-phishing protection.

- ⚡ **Serverless & Blazing Fast:** 100% running on the Cloudflare Edge network (Workers + D1 + KV). Zero VPS costs, millisecond global latency.

- 🔄 **Seamless Upgrade/Downgrade:** Cloud and Self-Hosted versions share a 1:1 identical SQL schema. Your data sovereignty is entirely in your hands.

- 🌍 **Native i18n:** Out-of-the-box support for 14 languages, from Chinese to Arabic, breaking down barriers for global developers.

- 🔑 **Progressive Security:** Passwords by default for backward compatibility, but administrators can seamlessly toggle on WebAuthn/Passkey enforcement per organization.

---

## ⚡ Quick Start: One-Click Deploy (Under 60 Seconds)

Deploy your own serverless SSO instance instantly. No terminal, no local environment setup required. We use GitHub Actions to automate everything.

1. Click the **"Actions"** tab at the top of this repository.

2. Select **"Deploy Nexus (One-Click Setup)"** from the left sidebar.

3. Click the **"Run workflow"** button on the right.

4. Input your **Cloudflare API Token** (requires `Edit Workers`, `Edit D1`, `Edit KV` permissions).

5. Set a **Custom Password** (this will be used for the initial `/setup` page and decrypting your secrets).

6. Hit **Run workflow**.

**What happens behind the scenes?**

- Automatically provisions your Cloudflare D1 database and KV namespace.

- Generates a cryptographically secure JWT secret.

- Builds and deploys the Worker.

- Executes the database schema.

- Generates an **encrypted ZIP** containing your database IDs and secrets (Download it from the Action Run Summary).

---

## 🏗️ Dual-Track Architecture

Nexus is built with data sovereignty at its core.

### ☁️ Cloud Edition (Serverless)
Powered by Cloudflare Workers, D1, and KV. 

Zero maintenance, zero costs. Perfect for indie hackers and minimalists. Just deploy and forget.

### 🐳 Self-Hosted Edition (Coming Soon)
Golang + Vue 3 + PostgreSQL + Docker.

Absolute data control. Perfect for enterprise intranets or NAS enthusiasts who demand complete isolation.

**Magic Promise:** Whether you run in the cloud or on-premises, the database schema remains 1:1 mirrored. Migrating your data is literally a `dump` and `import` away.

---

## 🛡️ Security & Compliance

We take security seriously. Nexus strictly adheres to standard SQL (ANSI SQL) with no proprietary dialects, ensuring true portability.

- **AGPL-3.0 Licensed:** Protects the community from unauthorized closed-source commercial exploitation.

- **Responsible Disclosure:** We maintain our own security advisory system (CSA). Read our [Security Policy](SECURITY.md) for more details.

- **Hardware Key Native:** We highly recommend using FIDO2 hardware keys (like YubiKey) to lock down your Nexus admin account.

---

## 🤝 Contributing & CLA

We welcome contributions from developers of all skill levels! 

To keep Nexus sustainable and offer enterprise versions, all contributors must sign our **Contributor License Agreement (CLA)**. 

- **You keep your copyright**, but grant CrCLARE Studio a perpetual license to use your contribution.

- **Perks:** If your PR contains significant core logic (100+ lines of functional code), you will receive a **Lifetime Free Nexus Pro License**. Your name will be permanently credited in the Git history and file headers.

Please read our [Contributing Guide](CONTRIBUTING.md) and sign the CLA when prompted by our bot.

---

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. 
See the [LICENSE](LICENSE) file for details.

*For commercial closed-source use or to obtain an AGPL waiver, please contact CrCLARE Studio for a Business License.*

---
<div align="center">
  <i>"Create Wonderful Code, Build A Wonderful World."</i><br>
  <b>© 2026 CrCLARE Studio. Here We Go.</b>
</div>
