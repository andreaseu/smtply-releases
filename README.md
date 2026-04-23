# SMTPly Releases

Öffentliche Installer-Downloads für **SMTPly** — dem lokalen SMTP-Relay für Microsoft 365.

## Was ist SMTPly?

SMTPly nimmt klassische SMTP-E-Mails auf Ihrem Windows-Server an und leitet sie per OAuth2 und Microsoft Graph über Ihr Microsoft 365 weiter — ganz ohne Cloud-Zwischenstopp und ohne Datenweitergabe.

Typische Anwendungsfälle: Drucker, Scanner, ERP-Systeme, CRM-Software, Hotelsoftware, Monitoring-Tools und Eigenentwicklungen, die weiterhin klassisches SMTP verwenden und von der kommenden Basic-Auth-Abschaltung in Exchange Online betroffen sind.

- **Produktseite:** <https://smtply.hpn.io>
- **Direkt-Download aktuelle Version:** <https://smtply.hpn.io/dl/latest>
- **Changelog:** siehe [Releases](https://github.com/andreaseu/smtply-releases/releases)

## Installation

1. Installer als Administrator ausführen
2. Setup-Wizard durchlaufen
3. Azure-App-Registrierung eintragen (siehe [Schritt-für-Schritt-Anleitung](https://smtply.hpn.io/support.html#azure-setup))
4. Windows-Dienst startet automatisch

## Upgrade

Neueren Installer einfach ausführen — die App wird drüber installiert.
Konfiguration, Logs und Lizenz bleiben erhalten. Ab Version 1.3.0 weist die App selbständig auf neue Versionen hin und zeigt die Release-Notes direkt im „Über"-Bereich an.

## Systemanforderungen

- Windows 10/11 oder Windows Server 2016/2019/2022/2025 (x64)
- Administrator-Rechte für die Installation
- ca. 81 MB (self-contained .NET 8 Runtime inklusive)

## Sicherheit

Bitte Sicherheitslücken nicht über öffentliche Issues melden — stattdessen:
- Kontakt: `mail@hpn.io`
- Details: [SECURITY.md](SECURITY.md)

## Hinweis

Der Quellcode lebt in einem separaten privaten Repository.
Dieses Repo dient ausschließlich der öffentlichen Bereitstellung der Installer-Downloads und Release Notes.