# Create Grid with ApptiveGrid

Creates a new grid in ApptiveGrid.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/users/:user_id/spaces/:space_id/grids`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Create Grid](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#addGrid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The grid name. |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
