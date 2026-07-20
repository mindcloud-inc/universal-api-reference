# Update Dashboard Positions with Instructure

Updates dashboard positions in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/dashboard_positions`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Dashboard Positions](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_dashboard_positions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboard_positions` | body | `object` | no | Object mapping dashboard asset strings to positions. |
