# List Notifications with DataScope Forms

Retrieves notifications from DataScope Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/external/notifications`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [List Notifications](https://dscope.github.io/docs/#list-last-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | End of the date range to fetch notifications for. |
| `start` | query | `string` | no | Start of the date range to fetch notifications for. |
