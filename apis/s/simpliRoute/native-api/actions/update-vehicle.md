# Update Vehicle with SimpliRoute

Updates an existing vehicle in SimpliRoute.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/routes/vehicles/:vehicle_id/`
- **Base URL:** `https://api.simpliroute.com`
- **Official documentation:** [Update Vehicle](https://documentation.simpliroute.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacity` | body | `number` | no | Optional updated capacity. |
| `license_plate` | body | `string` | no | Optional updated license plate. |
| `name` | body | `string` | no | Optional updated vehicle name. |
| `reference_id` | body | `string` | no | Optional updated reference ID. |
| `vehicle_id` | path | `number` | yes | The SimpliRoute vehicle ID. |
