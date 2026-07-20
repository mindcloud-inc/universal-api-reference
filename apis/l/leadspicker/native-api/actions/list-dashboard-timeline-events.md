# List Dashboard Timeline Events with Leadspicker

Retrieves dashboard timeline events from Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/dashboard/logs`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [List Dashboard Timeline Events](https://app.leadspicker.com/app/sb/api/docs#/Dashboard/apps_salesbooster_api_dashboard_logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Dashboard logs page number. |
| `page_size` | query | `number` | no | Dashboard logs page size. |
| `search` | query | `string` | no | Search dashboard logs. |
| `event_types` | query | `string<string>` | no | Comma-separated event types to include. |
