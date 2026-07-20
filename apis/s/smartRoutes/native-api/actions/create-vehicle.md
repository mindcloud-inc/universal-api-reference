# Create Vehicle with SmartRoutes

## Endpoint

- **Method:** `POST`
- **Path:** `/vehicles`
- **Base URL:** `https://api.smartroutes.io/v2`
- **Official documentation:** [Create Vehicle](https://api.smartroutes.io/v2/docs/api/#tag/Vehicles/paths/~1vehicles/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the vehicle. |
| `availability` | body | `string` | yes | Availability status of the vehicle. Accepted values: `0`, `1`, `2`. |
| `start_location` | body | `string` | yes | Location type where the vehicle starts. Accepted values: `0`, `1`, `2`. |
| `end_location` | body | `string` | yes | Location type where the vehicle ends. Accepted values: `0`, `1`. |
