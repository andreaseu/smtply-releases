# Security Policy

## Supported Versions

Only the latest SMTPly release receives security updates.

| Version | Supported |
| ------- | --------- |
| Latest  | Yes       |
| Older   | No        |

The current latest release is visible in the [Releases](https://github.com/andreaseu/smtply-releases/releases) tab.

## Reporting a Vulnerability

**Please do not open public GitHub issues for security vulnerabilities.**

If you have found a security issue in SMTPly, report it privately by email:

- **Contact:** `mail@hpn.io`
- **Subject:** `SMTPly Security — <brief topic>`

Include in your report:

- Affected SMTPly version (e.g. `1.1.0`)
- Windows version and architecture
- A clear description of the issue and the potential impact
- Reproduction steps or proof-of-concept (if available)
- Suggested mitigation or fix (if known)

## Response Timeline

- **Initial acknowledgement:** within 3 business days
- **Triage and severity assessment:** within 7 business days
- **Fix release:** depending on severity — critical issues are prioritised for an out-of-band release; low-severity issues ship with the next regular release

## Coordinated Disclosure

We follow a coordinated disclosure approach:

1. Reporter sends the initial report.
2. We confirm, investigate and develop a fix.
3. A release containing the fix is published.
4. After release, the reporter and we jointly publish details of the issue (e.g. in a security advisory on this repository).
5. Credit is given to the reporter unless anonymity is requested.

Please allow us a reasonable period (typically 30–90 days, depending on complexity) before publicly disclosing the issue.

## Scope

In scope:

- The SMTPly Windows service (`Smtply.Service.exe`)
- The SMTPly configuration GUI (`Smtply.exe`)
- The Inno Setup installer (`SMTPly-Setup-*.exe`)
- Cryptographic handling (DPAPI usage, OAuth2 token storage, SQLite field-level encryption)
- Named-pipe IPC between service and GUI
- License validation logic

Out of scope:

- Vulnerabilities in Microsoft 365, Microsoft Graph API or Azure AD / Entra ID — please report these to Microsoft directly
- Vulnerabilities in third-party dependencies (report upstream and notify us)
- Issues that require local administrator privileges to exploit (this is the service's normal operating context)
- Social-engineering or physical-access attacks

## Public Security Advisories

Published advisories will appear under the [Security Advisories](https://github.com/andreaseu/smtply-releases/security/advisories) tab of this repository.

## PGP

PGP-encrypted reports are optional. If you need our key, request it via the contact email above.

---

**Legal note:** The source code of SMTPly is maintained in a separate private repository.
This public repository contains only release binaries, release notes and this security policy.