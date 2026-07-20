# List Spaces with ApptiveGrid

Retrieves spaces from ApptiveGrid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/spaces`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Spaces](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#spaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | ApptiveGrid user ID. Use the ID returned by Get Current User. |
