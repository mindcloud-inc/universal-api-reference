# List Space Hooks with ApptiveGrid

Retrieves hooks from an ApptiveGrid space.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/hooks`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Space Hooks](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
