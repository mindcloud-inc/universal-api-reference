# UptimeRobot: Native API Reference

A consolidated summary of UptimeRobot's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://uptimerobot.com/api/legacy/
- **API base URL:** `https://api.uptimerobot.com/v2`

## Authentication

### API Key

Authenticate with a UptimeRobot legacy API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://uptimerobot.com/api/legacy/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Maintenance Window](actions/create-maintenance-window.md) | `POST /newMWindow` | [docs](https://uptimerobot.com/api/legacy/) |
| [Create Monitor](actions/create-monitor.md) | `POST /newMonitor` | [docs](https://uptimerobot.com/api/legacy/) |
| [Delete Maintenance Window](actions/delete-maintenance-window.md) | `POST /deleteMWindow` | [docs](https://uptimerobot.com/api/legacy/) |
| [Delete Monitor](actions/delete-monitor.md) | `POST /deleteMonitor` | [docs](https://uptimerobot.com/api/legacy/) |
| [Get Account Details](actions/get-account-details.md) | `POST /getAccountDetails` | [docs](https://uptimerobot.com/api/legacy/) |
| [Get Alert Contacts](actions/get-alert-contacts.md) | `POST /getAlertContacts` | [docs](https://uptimerobot.com/api/legacy/) |
| [Get Maintenance Windows](actions/get-maintenance-windows.md) | `POST /getMWindows` | [docs](https://uptimerobot.com/api/legacy/) |
| [Get Monitors](actions/get-monitors.md) | `POST /getMonitors` | [docs](https://uptimerobot.com/api/legacy/) |
| [Get Public Status Pages](actions/get-public-status-pages.md) | `POST /getPSPs` | [docs](https://uptimerobot.com/api/legacy/) |
| [Reset Monitor](actions/reset-monitor.md) | `POST /resetMonitor` | [docs](https://uptimerobot.com/api/legacy/) |
| [Update Alert Contact](actions/update-alert-contact.md) | `POST /editAlertContact` | [docs](https://uptimerobot.com/api/legacy/) |
| [Update Maintenance Window](actions/update-maintenance-window.md) | `POST /editMWindow` | [docs](https://uptimerobot.com/api/legacy/) |
| [Update Monitor](actions/update-monitor.md) | `POST /editMonitor` | [docs](https://uptimerobot.com/api/legacy/) |
| [Update Public Status Page](actions/update-public-status-page.md) | `POST /editPSP` | [docs](https://uptimerobot.com/api/legacy/) |
