# List Grid Virtual Grids with ApptiveGrid

Retrieves virtual grids from an ApptiveGrid grid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/grids/:grid_id/virtualgrids`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Grid Virtual Grids](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#virtualGrids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grid_id` | path | `string` | yes | The ApptiveGrid grid id. |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
