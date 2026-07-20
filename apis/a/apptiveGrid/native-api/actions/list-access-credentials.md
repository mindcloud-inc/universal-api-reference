# List Access Credentials with ApptiveGrid

Retrieves access credentials from ApptiveGrid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/:user_id/accessKeys`
- **Base URL:** `https://app.apptivegrid.de`
- **Official documentation:** [List Access Credentials](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#accessCredentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | ApptiveGrid user ID. Use the ID returned by Get Current User. |
