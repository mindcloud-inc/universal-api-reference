# List User Notifications with Zeplin

Retrieves a list of user notifications from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/me/notifications`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List User Notifications](https://docs.zeplin.dev/reference/getusernotifications)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_read` | query | `boolean` | no | Whether the notification is read or not |
| `type[]` | query | `array<string>` | no | Filter by type Example: `?type=project.extension&type=styleguide.extension` |
