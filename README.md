# Awesome-Enterprise-Password-Management-Privileged-Access

## Top Enterprise Password Management & Privileged Access Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Secrets Vaulting, Just-in-Time Access & Self-Hosted PAM Bastions*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Password Management & Privileged Access**. These tools help organizations secure credentials and control access to critical systems—covering everything from team password vaults with end-to-end encryption to full privileged access management (PAM) platforms with session recording, approval workflows, and zero-standing-privilege models.

**Examples** include 1Password Business, Bitwarden Enterprise, CyberArk, BeyondTrust, Delinea, JumpServer, Passbolt, Teleport, and Vaultwarden (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted password vaults, open-source PAM platforms, and community-driven privileged access control—ideal for organizations seeking data sovereignty and avoiding per-user SaaS pricing that compounds across headcount. The open-source landscape splits into **team password managers** (Passbolt, Vaultwarden, Padloc) for credential sharing, and **PAM/bastion platforms** (JumpServer, Teleport, Apache Guacamole) for brokered infrastructure access with session recording .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Company Size / Valuation / Revenue | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|------------------------------------|-------------------|--------------------------|
| **[CyberArk](https://www.cyberark.com/)** | **Enterprise PAM leader** with privileged session management, secrets management, and endpoint privilege security. Positioned for large organizations with complex compliance requirements. | **~$22.5B - $25B valuation** (Acquired by Palo Alto Networks for ~$25B; ~$1.36B revenue) | Privilege Cloud: Starting at **~$600 - $1,500/user/year** (annual enterprise commitments often starting at ~$30,000+) | **No self-service free tier**; 14 to 30-day guided Proof of Concept (PoC) evaluation available via enterprise sales. |
| **[Zoho Vault](https://www.zoho.com/vault/)** | Password management within the Zoho ecosystem. Affordable per-user pricing with sharing and audit trails. | **~$12.5B valuation** (Zoho Corp; ~$1.4B - $1.5B annual revenue) | Standard: **$0.90/user/month** (billed annually) or $1.00/user/month (monthly); Professional: **$4.00/user/month** (annual) | **Free forever plan**: 1 user only, unlimited passwords and passkeys across unlimited devices, 2 MB attachment limit (no team sharing/admin controls). 15-day free trial for paid tiers. |
| **[1Password Business](https://1password.com/)** | Enterprise password manager with travel mode, granular permissions, and breach monitoring. Positioned for organizations wanting polished UX and strong admin controls. | **~$6.8B valuation** (~$500M+ ARR) | Teams Starter: **$24.95/month** (flat rate up to 10 users); Business: **$8.99/user/month** (billed annually) | **14-day free trial** (full business feature set; no permanent free tier). |
| **[BeyondTrust](https://www.beyondtrust.com/)** | PAM platform with privileged remote access, password safe, and endpoint privilege management. | **~$1.5B+ valuation** (~$400M - $500M ARR; Francisco Partners PE-backed) | Privileged Remote Access: Starting at **~$2,000+/named user/year** (or ~$1,995/month base packages; typical entry contracts ~$17,000+/year) | **14-day free trial** (available for Remote Support / Privileged Remote Access; demo/PoC required for Password Safe). |
| **[Delinea (Secret Server)](https://delinea.com/)** | Enterprise secrets management and PAM. Formerly Thycotic. Focused on vaulting, rotation, and session management. | **~$1B+ valuation** (~$400M ARR; TPG Capital / Insight Partners PE-backed) | Secret Server Cloud: Starting at **~$8 - $12/user/month** (billed annually; platform entry minimums often apply) | **30-day free trial** (up to 10 users in cloud environment; no permanent free tier). |
| **[Bitwarden](https://bitwarden.com/)** | **Best open-source-rooted password manager for teams.** Open-source codebase with zero-knowledge encryption, third-party audits almost every year since 2018. Enterprise adds SCIM provisioning, custom roles, SSO, and free family plans for users. | **Private (~$100M+ funding raised)** (Fast-growing private entity backed by PSG & Battery Ventures) | Teams: **$4/user/month** (annual); Enterprise: **$6/user/month** (annual) | **Free forever plan**: Unlimited vault items, 2-user sharing with 1 organization, 2-step login, sync across unlimited devices. Paid plans offer a 7-day free trial. |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** | [![Stars](https://img.shields.io/github/stars/dani-garcia/vaultwarden?style=social&color=white)](https://github.com/dani-garcia/vaultwarden/stargazers) | **The community default for self-hosted password management.** Lightweight Rust implementation of the Bitwarden server API—works with all official Bitwarden clients. **Very low resource footprint, easy setup** . **Trade-off**: community-supported (no vendor SLA), and enterprise features like SSO/LDAP are not native . **Best for personal use and small teams** wanting Bitwarden's ecosystem without cloud dependency . |
| **[Passbolt](https://github.com/passbolt/passbolt_api)** | [![Stars](https://img.shields.io/github/stars/passbolt/passbolt_api?style=social&color=white)](https://github.com/passbolt/passbolt_api/stargazers) | **Security-first team password manager with PGP end-to-end encryption.** **The server never sees plaintext credentials**—every secret is encrypted with the recipient's public key before leaving the browser . **Community Edition is fully free with unlimited users and all sharing features** . Browser extension, CLI, REST API, and mobile apps (Pro tier). **Fine-grained permissions** (read-only vs. update per user per password) and SOC2-aligned audit log . **Trade-off**: UI is less polished than Bitwarden clones; onboarding non-technical users requires explaining GPG concepts . **Best for security-conscious teams** where cryptographic guarantees and auditability matter most . |
| **[Padloc](https://github.com/padloc/padloc)** | [![Stars](https://img.shields.io/github/stars/padloc/padloc?style=social&color=white)](https://github.com/padloc/padloc/stargazers) | **The most polished UI among self-hosted password managers.** Modern interface that wouldn't look out of place next to commercial offerings—designed for non-technical users . **Self-contained Docker image** (no external database required by default). End-to-end encryption with AES-GCM. **Free tier covers everything an individual or small family needs** . **Trade-off**: smaller community and ecosystem than Vaultwarden; enterprise features minimal . **Best for teams that need non-technical users to actually adopt the tool** . |
| **[JumpServer](https://github.com/jumpserver/jumpserver)** | [![Stars](https://img.shields.io/github/stars/jumpserver/jumpserver?style=social&color=white)](https://github.com/jumpserver/jumpserver/stargazers) | **The closest open-source approximation of a commercial PAM suite.** GPL-3.0 with paid Enterprise edition. **Brokers access to SSH, RDP, databases, and Kubernetes**, records sessions, **stores and manages credentials in a built-in vault**, and provides a web console for access requests and approvals . **Broadest built-in feature set of fully open-source PAM tools**—includes vaulting and approvals many alternatives lack . **Trade-off**: a single high-value target that must be hardened carefully; documentation and community strongest in Chinese . **Best for organizations wanting PAM + vaulting + recording in one open-source package** . |
| **[Teleport](https://github.com/gravitational/teleport)** | [![Stars](https://img.shields.io/github/stars/gravitational/teleport?style=social&color=white)](https://github.com/gravitational/teleport/stargazers) | **Modern identity-aware access for SSH, Kubernetes, databases, and apps.** Replaces bastion hosts, VPNs, and shared SSH keys with certificate-based, short-lived access tied to identity . **Community Edition is free to self-host** (some features moved to paid tiers). **Best for DevOps and SRE teams** wanting just-in-time access without a full commercial PAM contract . |
| **[Apache Guacamole](https://github.com/apache/guacamole-server)** | [![Stars](https://img.shields.io/github/stars/apache/guacamole-server?style=social&color=white)](https://github.com/apache/guacamole-server/stargazers) | **Clientless remote desktop gateway for browser-based SSH, RDP, and VNC.** Fully open-source (Apache 2.0), widely deployed. **No client software or plugins required**—administrators reach servers through the browser. Session recording for RDP and other protocols. Pluggable authentication (LDAP, SAML, TOTP) . **Trade-off**: not a full PAM suite—no vaulting or credential discovery; security depends heavily on how you deploy and authenticate it . **Best for lightweight bastion access** when you need browser-based access without a commercial PAM . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[ShellWarden](https://github.com/Boreas37/shellwarden)** | [![Stars](https://img.shields.io/github/stars/Boreas37/shellwarden?style=social&color=white)](https://github.com/Boreas37/shellwarden/stargazers) | **Self-hosted PAM platform with web SSH, RDP, and full session recording.** Go-based. Features: **AES-256-GCM encrypted credentials**, SSH Certificate Authority (short-lived certs, no static secrets on hosts), MFA (TOTP), RBAC (admin/operator/auditor), **JIT access approval** (time-boxed grants), OIDC/SSO, **append-only hash-chained audit log**, asciinema session recording with live shadowing, and SFTP file browser . **Best for teams wanting a modern, self-contained PAM bastion** with strong audit and approval features . |
| **[HashiCorp Boundary](https://github.com/hashicorp/boundary)** | [![Stars](https://img.shields.io/github/stars/hashicorp/boundary?style=social&color=white)](https://github.com/hashicorp/boundary/stargazers) | **Identity-based access to infrastructure without distributing credentials.** Users authenticate through an IdP; Boundary authorizes access to specific targets and can inject credentials brokered from HashiCorp Vault. **Community Edition free to self-host** (Business Source License since 2023—source-available, not OSI open source) . **Session recording in paid tiers** . **Best for teams already invested in HashiCorp Vault** wanting dynamic, just-in-time access . |
| **[Teampass](https://github.com/nilsteampassnet/TeamPass)** | [![Stars](https://img.shields.io/github/stars/nilsteampassnet/TeamPass?style=social&color=white)](https://github.com/nilsteampassnet/TeamPass/stargazers) | **Long-running PHP/MySQL self-hosted password manager for IT departments.** Browser-only interface with **per-folder permissions**. Slots into existing LAMP infrastructure without a new tech stack . **Trade-off**: server-side encryption (not end-to-end), dated UI . **Best for sysadmin teams** already running LAMP who want folder-based credential sharing . |

**Frameworks for building custom systems**: Choose **Passbolt** for cryptographic end-to-end encryption with fine-grained sharing , **Vaultwarden** for the lightest self-hosted Bitwarden-compatible server , or **Padloc** for the most user-friendly UI —all without per-user SaaS fees. For **PAM and infrastructure access**, **JumpServer** provides the broadest open-source feature set (vaulting + recording + approvals) , while **ShellWarden** offers a modern Go-based alternative with strong audit trails .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Password managers and PAM platforms handle the keys to your entire infrastructure; enforce strong master passwords, MFA, and regular backups of encrypted vaults. **A lost master password or corrupted vault can lock you out permanently**—store recovery kits securely offline.
- **Open-source password management splits into two categories with very different threat models.** **Team password managers** (Passbolt, Vaultwarden, Padloc) protect shared credentials with end-to-end encryption—Passbolt's PGP model means the server never sees plaintext , Vaultwarden is the lightest Bitwarden-compatible option , and Padloc prioritizes usability . **PAM/bastion platforms** (JumpServer, Teleport, ShellWarden) broker access to servers and record sessions—these are **high-value targets** that must be hardened carefully . **Licensing matters**: **HashiCorp Boundary moved to Business Source License** (source-available, not OSI open source) , **JumpServer is GPL-3.0 with a paid Enterprise edition** , and **Passbolt is AGPL-3.0** . **Validate whether you need credential sharing (Passbolt) or infrastructure access control (JumpServer)** —they solve different problems despite overlapping terminology.

---

**Made for security engineers, IT administrators, and organizations building credential and access infrastructure.**  
Let's make enterprise password management and privileged access more open, auditable, and secure.
