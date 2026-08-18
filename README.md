# X1 Panel

X1 Panel is a self-hosted administration and remote configuration platform designed for compatible X1/XCIPTV applications.

It provides a centralized interface for application configuration, portals, devices, profiles, themes, languages, VPN, external services, APK management, backups, monitoring and administrative operations.

The panel interface is available in **English and Portuguese**.

---

## Features

### Application Management

* Up to 5 configurable portals
* Portal names and URLs
* Theme selection
* Application language selection
* Visual Home Editor
* Feature Manager
* Player configuration
* Stream configuration
* Custom logo
* Custom intro video
* Parental controls
* Notifications
* Application update settings

### Feature Manager

Application features can be remotely enabled or disabled.

Supported controls include:

* Live TV
* EPG
* Movies
* Series
* Catch-up
* Radio
* Favorites
* Multi-screen
* Account
* VPN
* Recording
* Parental controls
* Notifications
* Updates
* Registration
* Messages
* Announcements
* AdMob
* VAST
* Prebid
* Player hardware options
* Subtitles

Each portal can also have its own feature configuration.

---

## Visual Home Editor

The Visual Home Editor provides a representation of the application's main screen.

Administrators can configure:

* Theme
* Language
* Portal
* Home modules
* VPN
* Recording
* Parental controls
* Notifications
* Update options

Only settings supported by the application are written to the application configuration.

---

## Device Management

X1 Panel tracks devices communicating with the API.

Available information includes:

* User ID
* Device ID
* IP address
* Application version
* Package information
* Last connection
* Online activity
* Assigned profile
* License status

Administrators can:

* Search devices
* Filter devices
* Block devices
* Activate devices
* Suspend devices
* Define expiration dates
* Add internal notes
* Apply profiles
* Perform bulk actions

---

## Licenses

Device-specific license rules can be configured.

Available states include:

* Active
* Blocked
* Suspended
* Expired

Expiration can also be handled automatically based on a configured date.

---

## Profiles

Profiles allow different devices to receive different application configurations.

A profile can override:

* Theme
* Language
* Portal
* Portal name
* Player settings
* Application features
* VPN settings
* Interface options

Each option supports:

* Inherit
* Enable
* Disable

This allows profiles to override only selected values while continuing to inherit the global X1 configuration.

### Included Presets

* Full
* Minimal
* IPTV Only
* Kids

Profiles can also be cloned and customized.

---

## VPN

X1 Panel includes VPN configuration management.

VPN entries can be managed from the administration interface and delivered to compatible applications through the API.

---

## Sports

The Sports module supports configurable providers.

Available modes include:

* TVSportGuide compatibility mode
* TheSportsDB
* Custom URL / iframe provider

Provider credentials and configuration can be changed directly from the panel.

---

## TMDB

The TMDB module provides configuration and integration tools for supported movie and backdrop functionality.

---

## Messages and Announcements

X1 Panel supports:

* Global announcements
* User-specific messages
* Message configuration
* Device-targeted communication

---

## APK Management

The APK update system provides:

* Direct APK upload
* Version Code management
* Auto Update configuration
* Published APK URL
* SHA-256 calculation
* Version history
* Rollback

Before replacing the currently published APK, X1 Panel can automatically archive the previous version.

---

## APK Version Rollback

Previous APK versions are stored with:

* Version Code
* Date
* File size
* SHA-256

An archived APK can be restored directly from the administration panel.

The currently published version is archived before rollback.

---

## APK Laboratory

APK Lab helps administrators verify communication between the panel and connected devices.

It tracks:

* `licV3` delivery
* `licV4` delivery
* `connv2` callbacks
* Configuration fingerprint
* Delivered theme
* Delivered language
* Assigned profile
* APK version
* Last callback

The panel distinguishes between:

**Configuration delivered by the server**

and

**Function visually confirmed on a real Android device**

### Android Validation Checklist

Tests can be manually marked as:

* PASS
* FAIL
* N/A

Available validation items include:

* Theme
* Language
* Menus
* Portal
* Players
* VPN
* Messages
* Announcements
* Logo
* Intro
* Sports
* TMDB
* Update
* Parental Control

---

## Cloud Backup

The client application Cloud Backup endpoint is supported separately from X1 Panel backups.

---

## X1 Panel Backup

The administration panel includes its own backup and restore system.

Backups can include:

* Global configuration
* Devices
* Licenses
* Profiles
* Messages
* VPN configuration
* Logs
* Administrative state
* Logo
* Intro
* Additional settings

X1 backups use the `.x1backup` format.

---

## Migration Assistant

The Migration Assistant can analyze data from a previous compatible panel installation before importing it.

The migration process uses two stages:

1. Analyze
2. Apply

The report identifies each component as:

* READY
* MISSING
* CONFLICT
* ACTION REQUIRED

Supported migration sources can include:

* `main.json`
* `connv2.json`
* Device databases
* VPN databases
* Message databases
* TMDB configuration
* Sports configuration
* Logo
* Intro

A complete X1 backup is created before migration changes are applied.

---

## Dashboard

The operational dashboard provides information about:

* Connected devices
* Recently active devices
* Blocked licenses
* Expired licenses
* API requests
* API errors
* Error rate
* Response latency
* APK version
* Alerts
* Notifications
* Open operational tasks
* Health Check status

---

## Diagnostics

X1 Diagnostics verifies important parts of the installation.

Checks include:

* PHP
* OpenSSL
* Writable storage
* Main configuration
* Required application parameters
* API endpoints
* Cloud Backup
* Logo
* Intro
* Published APK
* Portal connectivity

---

## Health Checks

Health Checks can be executed:

* Manually
* Through a protected cron endpoint

Each run can be stored in the health history.

A protected token is used for automated cron execution.

---

## Alerts

The Alert Center can detect conditions such as:

* High API error rate
* Expired licenses
* Missing APK
* Storage permission problems
* OpenSSL problems
* Active maintenance mode
* Health Check failures

---

## Notifications

Persistent administrative notifications are generated for important events such as:

* APK upload
* APK rollback
* Health Check failures
* Operational events

---

## Operational Tasks

Administrators can create internal tasks with:

* Title
* Notes
* Due date
* Completion status

---

## Maintenance Mode

Maintenance mode can be:

* Enabled immediately
* Scheduled

Scheduled maintenance supports:

* Start date/time
* End date/time
* Custom maintenance message

Compatible API responses automatically reflect the active maintenance state.

---

## Team Management

X1 Panel supports multiple administrator accounts.

### Roles

* Owner
* Admin
* Operator
* Read Only

Permissions are enforced by the backend.

Read Only accounts cannot modify data through direct POST requests.

---

## Security

X1 Panel includes:

* Password hashing
* CSRF protection
* Login rate limiting
* Temporary login lockout
* Session timeout
* Maximum session lifetime
* Session ID rotation
* HttpOnly cookies
* SameSite cookies
* Security headers
* Administrative auditing
* Optional 2FA / TOTP
* Optional administrator IP restrictions

---

## Two-Factor Authentication

TOTP-based two-factor authentication can be enabled individually for administrator accounts.

Compatible authenticator applications can be used.

The authentication flow is:

1. Username and password
2. TOTP verification
3. Administration dashboard

---

## Audit Log

Administrative actions are recorded.

Configuration changes can include before/after differences such as:

```text
app.theme: 2 -> 3
```

This makes configuration changes easier to trace.

---

## Interface Languages

The X1 administration interface supports:

* English
* Portuguese

The administration interface language is independent from the language configured for the client application.

---

## Requirements

Recommended environment:

* PHP 8.1 or newer
* OpenSSL
* Apache or Nginx
* HTTPS
* Required directory write permissions

Some migration functions may additionally require:

* PHP SQLite3
* PHP ZIP

---

## Installation

1. Upload X1 Panel to your web server.
2. Open the installation URL.
3. Run `install.php`.
4. Create the Owner account.
5. Log in to X1 Panel.
6. Configure your portals.
7. Configure application settings.
8. Configure the compatible application to use the X1 endpoints.
9. Run X1 Diagnostics.
10. Test the application on a real device.

---

## Main API Endpoints

```text
api/ApiIPTV.php
api/CloudBackup.php
```

Do not rename these endpoints unless the client application is updated accordingly.

---

## Updating X1 Panel

Before updating an existing installation:

1. Create an X1 Panel backup.
2. Keep a copy of the current installation.
3. Install the new files.
4. Run X1 Diagnostics.
5. Verify API functionality.
6. Test the connected application on a real Android device.

---

## Security Recommendations

For production installations:

* Use HTTPS
* Use a strong Owner password
* Enable 2FA
* Keep PHP updated
* Restrict server permissions
* Protect backups
* Do not expose sensitive configuration files
* Review audit logs regularly
* Create backups before major changes

---

## Community

### Telegram

https://t.me/+XkuQS_QuD6g4Nzc0

### Forum

https://forum.x1panel.space

### Discord

https://discord.gg/vSSw6jHmw

---

## Compatibility

Application behavior can differ between builds.

A setting being available in X1 Panel does not automatically guarantee that every application build implements that setting.

Use APK Lab and a real Android test device to validate compatibility before production deployment.

---

## Disclaimer

X1 Panel is a management and configuration platform.

Users are responsible for the servers, applications, content, credentials and external services they configure through the software.
