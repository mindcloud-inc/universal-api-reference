# Get Alerts with XenForo

Retrieves a list of user alerts from XenForo.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Get Alerts](https://docs.xenforo.com/api/get-alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unread` | query | `boolean` | no | If true, gets only unread alerts. |
| `unviewed` | query | `boolean` | no | If true, gets only unviewed alerts. |
