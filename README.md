# SMTPly — Local SMTP Relay for Microsoft 365 (Windows)

[![Latest release](https://img.shields.io/github/v/release/andreaseu/smtply-releases?label=latest%20release)](https://github.com/andreaseu/smtply-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-smtply.app%2Fdl%2Flatest-0b6cff)](https://smtply.app/dl/latest)

**English** · [Deutsche Version weiter unten ↓](#deutsch)

Official installer downloads for **SMTPly** — a Windows SMTP relay (smart host) that accepts classic SMTP mail from legacy devices and applications and forwards it to **Microsoft 365 / Exchange Online / Office 365** via **OAuth2 and the Microsoft Graph API**. No Basic Authentication, no cloud middleman, no data sharing — the relay runs entirely on your own Windows server.

**The problem it solves:** Microsoft has switched off Basic Auth for SMTP in Exchange Online. Printers, scanners, ERP and CRM systems, backup software, firewalls, NAS devices, monitoring tools, hotel and line-of-business applications that only speak plain SMTP can no longer send mail directly. SMTPly is the drop-in fix: point your devices at it and it handles the OAuth2 translation — a modern replacement for the deprecated IIS 6.0 SMTP service and for SMTP relaying through on-premises Exchange after a migration to Microsoft 365.

- **Website:** <https://smtply.app> · [English pages](https://smtply.app/en/)
- **Download latest version:** <https://smtply.app/dl/latest>
- **Changelog:** see [Releases](https://github.com/andreaseu/smtply-releases/releases)
- **Support & FAQ:** <https://smtply.app/en/support.html>

## Key features

- SMTP listener on port 25, 587 or any custom port — optional STARTTLS / implicit TLS, multiple listeners in parallel
- Delivery via Microsoft Graph `sendMail` — sent messages appear in the mailbox under **Sent Items**
- Messages are relayed **byte-for-byte**: headers, encodings, embedded images and attachments stay untouched
- Mail tracker, live system log, persistent retry queue with exponential backoff
- SMTP AUTH (optional or enforced, free-form usernames), IP allowlist, sender domain allowlist
- Business edition: multiple Microsoft 365 tenants, monitoring endpoint (`/health` + `/metrics` for PRTG, Zabbix, CheckMK, Prometheus), journal BCC to an archive mailbox
- GUI fully localized in **English and German** · 14-day fully functional trial

## Installation

1. Run the installer as administrator
2. Follow the setup wizard
3. Enter your Azure app registration ([step-by-step guide](https://smtply.app/en/support.html#azure-setup))
4. The Windows service starts automatically

## Upgrade

Simply run the newer installer over the existing installation — configuration, logs and license are preserved. Since version 1.3.0 the app notifies you about new versions and shows the release notes in the About section.

## System requirements

- Windows 10/11 or Windows Server 2016/2019/2022/2025 (x64)
- Administrator rights for installation
- approx. 82 MB (self-contained .NET 8 runtime included)

## Security

Please do not report security vulnerabilities via public issues:

- **Contact:** `mail@smtply.app`
- Details: [SECURITY.md](SECURITY.md)

---

<a id="deutsch"></a>

# SMTPly — Lokaler SMTP-Relay für Microsoft 365 (Windows)

Öffentliche Installer-Downloads für **SMTPly** — einen Windows-SMTP-Relay (Smarthost), der klassische SMTP-Mails von Legacy-Geräten und -Anwendungen entgegennimmt und per **OAuth2 über die Microsoft-Graph-API** an **Microsoft 365 / Exchange Online** weiterleitet. Ohne Basic Authentication, ohne Cloud-Zwischenstopp, ohne Datenweitergabe — der Relay läuft vollständig auf Ihrem eigenen Windows-Server.

**Das gelöste Problem:** Microsoft hat Basic Auth für SMTP in Exchange Online abgeschaltet. Drucker, Scanner, ERP- und CRM-Systeme, Backup-Software, Firewalls, NAS-Geräte, Monitoring-Tools, Hotel- und Branchensoftware, die nur klassisches SMTP sprechen, können nicht mehr direkt versenden. SMTPly ist der Drop-in-Ersatz: Geräte auf SMTPly zeigen lassen, die OAuth2-Übersetzung übernimmt der Dienst — der moderne Nachfolger für den abgekündigten IIS-6.0-SMTP-Service und für das Relaying über lokalen Exchange nach einer Migration zu Microsoft 365.

- **Website:** <https://smtply.app>
- **Aktuelle Version herunterladen:** <https://smtply.app/dl/latest>
- **Changelog:** siehe [Releases](https://github.com/andreaseu/smtply-releases/releases)
- **Support & FAQ:** <https://smtply.app/support.html>

## Funktionen

- SMTP-Listener auf Port 25, 587 oder frei wählbar — optional STARTTLS / implizites TLS, mehrere Listener parallel
- Versand über Microsoft Graph `sendMail` — Mails erscheinen im Postfach unter **Gesendete Elemente**
- Nachrichten werden **Byte für Byte** durchgereicht: Header, Kodierungen, eingebettete Bilder und Anhänge bleiben unverändert
- Mail-Tracker, Live-System-Log, persistente Retry-Queue mit exponentiellem Backoff
- SMTP-AUTH (optional oder erzwungen, frei wählbare Benutzernamen), IP-Whitelist, Absender-Domänen-Whitelist
- Business-Edition: mehrere Microsoft-365-Tenants, Monitoring-Endpoint (`/health` + `/metrics` für PRTG, Zabbix, CheckMK, Prometheus), Journal-BCC an ein Archiv-Postfach
- GUI vollständig in **Deutsch und Englisch** · 14 Tage voll funktionsfähig testen

## Installation

1. Installer als Administrator ausführen
2. Setup-Wizard durchlaufen
3. Azure-App-Registrierung eintragen ([Schritt-für-Schritt-Anleitung](https://smtply.app/support.html#azure-setup))
4. Windows-Dienst startet automatisch

## Upgrade

Neueren Installer einfach über die bestehende Installation ausführen — Konfiguration, Logs und Lizenz bleiben erhalten. Ab Version 1.3.0 weist die App selbständig auf neue Versionen hin und zeigt die Release-Notes im „Über"-Bereich an.

## Systemanforderungen

- Windows 10/11 oder Windows Server 2016/2019/2022/2025 (x64)
- Administrator-Rechte für die Installation
- ca. 82 MB (self-contained .NET 8 Runtime inklusive)

## Sicherheit

Bitte Sicherheitslücken nicht über öffentliche Issues melden:

- **Kontakt:** `mail@smtply.app`
- Details: [SECURITY.md](SECURITY.md)

---

**Note / Hinweis:** The SMTPly source code lives in a separate private repository — this repository only hosts the public installer downloads and release notes. · Der Quellcode liegt in einem separaten privaten Repository — dieses Repo dient ausschließlich der öffentlichen Bereitstellung der Installer und Release-Notes.
