# Get User Details with ApptiveGrid

Retrieves a user from ApptiveGrid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [Get User Details](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/User-class.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | ApptiveGrid user ID. Use the ID returned by Get Current User. |
