# Update User Notification Settings with Zeplin

Updates user notification settings in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/me/notifications`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update User Notification Settings](https://docs.zeplin.dev/reference/updateusernotifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type[]` | query | `array<string>` | no | Filter by type Example: `?type=project.extension&type=styleguide.extension` |
| `id[]` | query | `array<string>` | no | Filter by id Example: `?id=5fbe387f8c72ef23659fb500&id=602281f4783f72fccc045484` |
| `is_read` | body | `boolean` | yes | New is_read status for notifications |
