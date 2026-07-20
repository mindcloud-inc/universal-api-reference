# Create Space with ApptiveGrid

Creates a new space in ApptiveGrid.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/users/:user_id/spaces`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Create Space](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#addSpace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The space name. |
| `user_id` | path | `string` | yes | The ApptiveGrid user id. |
