# List Space Invitations with ApptiveGrid

Retrieves invitations from an ApptiveGrid space.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/invitations`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Space Invitations](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#invitations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
