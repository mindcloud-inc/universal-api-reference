# Create Vehicle with SimpliRoute

Creates a new vehicle in SimpliRoute.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/routes/vehicles/`
- **Base URL:** `https://api.simpliroute.com`
- **Official documentation:** [Create Vehicle](https://documentation.simpliroute.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacity` | body | `number` | yes | Vehicle capacity. |
| `default_driver` | body | `number` | no | Optional default driver ID. |
| `license_plate` | body | `string` | no | Optional license plate. |
| `location_end_address` | body | `string` | yes | Ending address for the vehicle. |
| `location_end_latitude` | body | `number` | yes | Latitude for the ending address. |
| `location_end_longitude` | body | `number` | yes | Longitude for the ending address. |
| `location_start_address` | body | `string` | yes | Starting address for the vehicle. |
| `location_start_latitude` | body | `number` | yes | Latitude for the starting address. |
| `location_start_longitude` | body | `number` | yes | Longitude for the starting address. |
| `name` | body | `string` | yes | Vehicle name. |
| `reference_id` | body | `string` | no | Optional external reference for the vehicle. |
