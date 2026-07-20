# Get Grid Details with ApptiveGrid

Retrieves a grid from ApptiveGrid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/grids/:grid_id`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Get Grid Details](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/Grid-class.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grid_id` | path | `string` | yes | The ApptiveGrid grid id. |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
