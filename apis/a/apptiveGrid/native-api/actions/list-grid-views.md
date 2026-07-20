# List Grid Views with ApptiveGrid

Retrieves views from an ApptiveGrid grid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id/grids/:grid_id/views`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Grid Views](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#views)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grid_id` | path | `string` | yes | The ApptiveGrid grid id. |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
