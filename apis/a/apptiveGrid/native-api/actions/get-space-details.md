# Get Space Details with ApptiveGrid

Retrieves a space from ApptiveGrid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces/:space_id`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Get Space Details](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/Space-class.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | The ApptiveGrid space id. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
