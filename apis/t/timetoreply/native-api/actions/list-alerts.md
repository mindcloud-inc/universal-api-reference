# List Alerts with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/reports/alerts`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [List Alerts](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `number` | no | Agent identifier to filter alerts. |
| `days` | query | `number` | no | Number of days of alerts to include. |
| `team` | query | `number` | no | Team identifier to filter alerts. |
