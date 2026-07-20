# Delete Space with ApptiveGrid

Deletes an existing space from ApptiveGrid.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/users/:user_id/spaces/:space_id`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Delete Space](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
