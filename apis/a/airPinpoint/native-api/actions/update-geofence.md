# Update Geofence with AirPinpoint

Updates an existing geofence in AirPinpoint.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/geofences/{geofence_id}`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [Update Geofence](https://airpinpoint.com/docs/geofences)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `geofence_id` | path | `string` | yes |
| `latitude` | body | `number` | no |
| `longitude` | body | `number` | no |
| `name` | body | `string` | no |
| `notifyDestination` | body | `string` | no |
| `notifyType` | body | `string` | no |
| `radius` | body | `number` | no |
| `trackableId[]` | body | `array<string>` | no |
| `webhookEnabled` | body | `boolean` | no |
| `webhookSecret` | body | `string` | no |
