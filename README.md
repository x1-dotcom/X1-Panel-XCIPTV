# X1 Panel v2.8.1

X1 Panel is a self-hosted administration and remote configuration platform for compatible X1/XCIPTV applications.

The panel provides device management, visual profiles, APK customization, portal management, VPN, Sports, TMDB, messages, backups, monitoring, APK versioning and administration tools from a single interface.

The administration interface is fully available in **English and Portuguese**.

## Highlights

- Premium operational dashboard with stronger visual hierarchy
- Full PT / EN administration interface
- Up to 5 configurable portals
- Visual Home Editor
- Feature Manager
- Theme and application language controls
- Device tracking, filters and bulk actions
- Per-device licenses, blocking, suspension and expiration
- Visual device profiles with Inherit / Enable / Disable overrides
- VPN management
- Sports providers: TVSportGuide, TheSportsDB and custom iframe/URL
- TMDB integration
- Messages and global announcements
- APK Lab with delivery/callback tracking and Android validation checklist
- Direct APK upload, version history and rollback
- X1 Panel backup / restore
- Migration Assistant
- Diagnostics and Health Checks
- Alerts, notifications and operational tasks
- Scheduled maintenance
- API logs and administrative audit
- Owner / Admin / Operator / Read Only roles
- Optional 2FA / TOTP and administrator IP restrictions

## Requirements

- PHP 8.1+
- OpenSSL
- Apache or Nginx
- HTTPS recommended
- Write permissions for required runtime directories

Optional migration features may require:

- PHP SQLite3
- PHP ZIP

## Installation

1. Download the latest X1 Panel package.
2. Extract it to your web server.
3. Open `install.php` in your browser.
4. Create the Owner account.
5. Sign in to X1 Panel.
6. Configure portals and application options.
7. Run X1 Diagnostics.
8. Test the connected application on a real Android device before production use.

## Main API Endpoints

```text
api/ApiIPTV.php
api/CloudBackup.php
```

Do not rename these endpoints unless the compatible client application is updated accordingly.

## Security

For production installations:

- Use HTTPS
- Use a strong Owner password
- Enable 2FA where possible
- Keep PHP updated
- Protect backups and runtime data
- Review audit logs regularly
- Create a backup before major changes

## Interface Languages

- English
- Portuguese

The administration interface language is independent from the language configured for the connected application.

## Branding

Login copyright uses the current server year automatically:

**Copyright © YEAR X1Tech Solutions SA. All Rights Reserved.**

## Community

**Telegram**  
https://t.me/+XkuQS_QuD6g4Nzc0

**Forum**  
https://forum.x1panel.space

**Discord**  
https://discord.gg/vSSw6jHmw

## Compatibility

Application behavior may differ between builds. Use APK Lab and a real Android test device to validate the features supported by your specific application build.

## Disclaimer

X1 Panel is a management and configuration platform. Users are responsible for the servers, applications, content, credentials and external services configured through the software.
