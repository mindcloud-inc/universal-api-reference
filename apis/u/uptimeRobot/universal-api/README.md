# <img src="https://images.mindcloud.co/apps/icons/ceaddfe9-0440-4090-84ea-b19182e0ad20-4_1776362970441.png" alt="UptimeRobot logo" width="28" height="28"> UptimeRobot: Universal API

Manage UptimeRobot monitors, alerts, maintenance windows, and status pages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uptimeRobot/latest
- **Category:** IT Operations / Observability
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uptimerobot.com
- **Vendor API docs:** https://uptimerobot.com/api/legacy/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details and monitor counts from UptimeRobot. |

### Alert Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Contacts](actions/get-alert-contacts.md) | GET | Retrieves alert contacts and details from UptimeRobot. |
| [Update Alert Contact](actions/update-alert-contact.md) | PUT | Updates an existing alert contact in UptimeRobot. |

### Maintenance Window

| Action | Method | Description |
| --- | --- | --- |
| [Create Maintenance Window](actions/create-maintenance-window.md) | POST | Creates a new maintenance window in UptimeRobot. |
| [Delete Maintenance Window](actions/delete-maintenance-window.md) | DELETE | Deletes an existing maintenance window from UptimeRobot. |
| [Get Maintenance Windows](actions/get-maintenance-windows.md) | GET | Retrieves maintenance windows and details from UptimeRobot. |
| [Update Maintenance Window](actions/update-maintenance-window.md) | PUT | Updates an existing maintenance window in UptimeRobot. |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST | Creates a new monitor in UptimeRobot. |
| [Delete Monitor](actions/delete-monitor.md) | DELETE | Deletes an existing monitor from UptimeRobot. |
| [Get Monitors](actions/get-monitors.md) | GET | Retrieves monitors and monitoring details from UptimeRobot. |
| [Reset Monitor](actions/reset-monitor.md) | PUT | Resets an existing monitor's stats and response times in UptimeRobot. |
| [Update Monitor](actions/update-monitor.md) | PUT | Updates an existing monitor in UptimeRobot. |

### Public Status Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Public Status Pages](actions/get-public-status-pages.md) | GET | Retrieves public status pages from UptimeRobot. |
| [Update Public Status Page](actions/update-public-status-page.md) | PUT | Updates an existing public status page in UptimeRobot. |

