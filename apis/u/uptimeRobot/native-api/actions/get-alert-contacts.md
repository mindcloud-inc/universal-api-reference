# Get Alert Contacts with UptimeRobot

Retrieves alert contacts and details from UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/getAlertContacts`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Get Alert Contacts](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alert_contacts` | body | `string` | no | Optional dash-separated alert contact IDs to filter. |
| `offset` | body | `number` | no | Pagination offset. |
| `limit` | body | `number` | no | Pagination limit, max 50. |
