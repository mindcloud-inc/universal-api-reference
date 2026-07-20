# List Space Grids with ApptiveGrid

Retrieves grids from an ApptiveGrid space.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/grids`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Space Grids](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#grids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
