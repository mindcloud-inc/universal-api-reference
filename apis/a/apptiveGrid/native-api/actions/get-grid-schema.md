# Get Grid Schema with ApptiveGrid

Retrieves a grid schema from ApptiveGrid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/grids/:grid_id/schema`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Get Grid Schema](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grid_id` | path | `string` | yes | The ApptiveGrid grid id. |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
