# List Notification Tasks with SmartRoutes

## Endpoint

- **Method:** `GET`
- **Path:** `/notification-tasks`
- **Base URL:** `https://api.smartroutes.io/v2`
- **Official documentation:** [List Notification Tasks](https://api.smartroutes.io/v2/docs/api/#tag/Notification-Tasks/paths/~1notification-tasks/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updated_at_min` | query | `date` | no | Only return notification tasks updated on or after this timestamp. |
| `status` | query | `string` | no | Filter notification tasks by status. |
| `type` | query | `string` | no | Filter notification tasks by type. |
