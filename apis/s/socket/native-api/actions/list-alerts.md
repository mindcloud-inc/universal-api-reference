# List Alerts with Socket

Retrieves latest organization alerts from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/alerts`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [List Alerts](https://docs.socket.dev/reference/alertslist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters.alertAction` | query | `list<string>` | no |
| `filters.alertCategory` | query | `list<string>` | no |
| `filters.alertKEV` | query | `boolean` | no |
| `filters.alertPriority` | query | `list<string>` | no |
| `filters.alertSeverity` | query | `list<string>` | no |
| `filters.alertStatus` | query | `string` | no |
| `filters.alertType` | query | `list<string>` | no |
| `per_page` | query | `number` | no |
| `startAfterCursor` | query | `string` | no |
