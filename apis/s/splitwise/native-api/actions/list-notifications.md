# List Notifications with Splitwise

Retrieves notifications from Splitwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_notifications`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [List Notifications](https://dev.splitwise.com/#tag/notifications/paths/~1get_notifications/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of notifications to return. Use 0 for the provider maximum. |
| `updated_after` | query | `date` | no | Only return notifications updated after this timestamp. |
