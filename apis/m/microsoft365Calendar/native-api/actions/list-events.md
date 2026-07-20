# List Events with Microsoft 365 Calendar

Retrieves events from Microsoft 365 Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/events`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Events](https://learn.microsoft.com/en-us/graph/api/user-list-events?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Number of events to return. |
