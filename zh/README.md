<div align="center">

# 🌌 Nexus

**现代 Web 的终极身份枢纽**

*欢迎来到充满无限可能的星系。*

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Status: Public Beta](https://img.shields.io/badge/Status-Public_Beta-orange.svg)](#)
[![Serverless](https://img.shields.io/badge/Serverless-Cloudflare_Workers-F38020?logo=cloudflare)](https://workers.cloudflare.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![JavaScript](https://img.shields.io/badge/JavaScript-100%25-yellow?logo=javascript)](https://github.com/CrCLARE/Nexus)

---

[English](./README.md) | [简体中文](./zh/README.md)

---

[官网](https://nexus.crclare.top) • [文档（尚未完成）](https://sso.crclare.top) • [报告 Bug](../../issues) • [请求新功能](../../issues)

</div>

---

## 🚀 Nexus 是什么？

**Nexus** 是一款由 **CrCLARE Studio** 开发的轻量级、100% 纯 JavaScript 编写的开源单点登录（SSO）平台。

专为零服务器成本和极致性能而设计，为您的生态注入企业级零信任安全。无论你是在构建 SaaS、私有论坛，还是只想给你的 [Twikoo](https://twikoo.js.org/) 博客评论区加上独一无二的“认证金标”，Nexus 都是你完美的数字身份底座。

> ⚠️ **注意：** Nexus 目前处于 **公测阶段（Public Beta）**。我们正在积极修复边界问题并优化 UI。欢迎通过 GitHub Issues 提供反馈！

---

## ✨ 为什么选择 Nexus？

摆脱厂商绑架，重新定义你的数字身份底座。

- 🛡️ **零信任安全：** 全面支持 WebAuthn/Passkey 硬件密钥（如 YubiKey、iCloud 通行密钥），实现物理级防钓鱼。

- ⚡ **极速 Serverless：** 100% 运行于 Cloudflare 边缘网络（Workers + D1 + KV）。零 VPS 成本，毫秒级全球延迟。

- 🔄 **无缝升级/降级：** 云端与自托管版本共享 1:1 的 SQL 数据库结构。你的数据主权随时由你掌控。

- 🌍 **原生多语言：** 开箱即用的 14 国语言支持，从中文到阿拉伯语，打破全球开发者的语言壁垒。

- 🔑 **渐进式安全：** 默认支持传统密码以保证向下兼容，但管理员可以按需无缝开启 WebAuthn/Passkey 强制验证。

---

## ⚡ 极速开始：一键部署（60 秒内完成）

瞬间部署你自己的 Serverless SSO 实例。无需终端，无需配置本地环境。我们使用 GitHub Actions 自动化处理一切。

1. 点击本仓库顶部的 **"Actions"** 标签页。

2. 在左侧边栏选择 **"Deploy Nexus (One-Click Setup)"**。

3. 点击右侧的 **"Run workflow"** 按钮。

4. 输入你的 **Cloudflare API Token**（需包含 `Edit Workers`、`Edit D1`、`Edit KV` 权限）。

5. 设置一个 **自定义密码**（这将用于初始的 `/setup` 页面以及解密你的凭证文件）。

6. 点击 **Run workflow** 运行。

**系统在后台为你做了什么？**

- 自动创建你的 Cloudflare D1 数据库和 KV 命名空间。

- 生成加密安全的 JWT 签名密钥。

- 构建并部署 Worker 代码。

- 自动执行数据库表结构初始化。

- 生成一个包含数据库 ID 和密钥的 **加密 ZIP 压缩包**（请在 Action 运行摘要页底部下载）。

---

## 🏗️ 双轨架构，数据主权归一

Nexus 的设计核心是数据主权。

### ☁️ 云端版（Serverless）

由 Cloudflare Workers、D1 和 KV 强力驱动。

零运维，零成本。适合独立开发者和极简主义者的首选。部署即忘。

### 🐳 自托管版（即将推出）

Golang + Vue 3 + PostgreSQL + Docker。

绝对的数据掌控权。适合企业内网、对数据隔离有极高要求的 NAS 玩家。

**魔法承诺：** 无论你在云端还是本地运行，数据库表结构始终保持 1:1 镜像。迁移你的数据，只差一次导出和导入的距离。

---

## 🛡️ 安全与合规

我们极其重视安全。Nexus 严格遵循标准 SQL（ANSI SQL），没有任何私有方言，确保真正的跨平台可移植性。

- **AGPL-3.0 开源协议：** 保护社区免受未经授权的闭源商业剥削。

- **负责任披露：** 我们维护着自己的安全公告体系（CSA）。详情请阅读我们的 [安全策略](SECURITY.md)。

- **原生硬件密钥：** 我们强烈建议使用 FIDO2 硬件密钥（如 YubiKey）来锁死你的 Nexus 管理员账号。

---

## 🤝 贡献与 CLA

欢迎所有技术水平的开发者参与贡献！

为了保证 Nexus 的可持续发展并提供企业版本，所有贡献者在提交 PR 前必须签署我们的 **贡献者许可协议（CLA）**。

- **您保留您的版权**，但授予 CrCLARE Studio 永久使用您贡献的许可。

- **贡献者福利：** 如果你的 PR 包含核心实质性代码逻辑（100 行以上的功能性代码），你将获得一份 **永久免费的 Nexus Pro 授权**。你的名字将永久保留在 Git 历史和文件头中。

请阅读我们的 [贡献指南](CONTRIBUTING.md)，并在机器人提示时签署 CLA。

---

## 📄 开源协议

本项目基于 **GNU Affero General Public License v3.0 (AGPL-3.0)** 协议开源分发。
详情请参阅 [LICENSE](LICENSE) 文件。

*如需用于闭源商业项目，或需要豁免 AGPL 协议，请联系 CrCLARE Studio 获取商业授权（Business License）。*

---
<div align="center">
  <i>"Create Wonderful Code, Build A Wonderful World."</i><br>
  <b>© 2026 CrCLARE Studio. Here We Go.</b>
</div>
