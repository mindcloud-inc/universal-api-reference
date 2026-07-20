# Create Geofence with AirPinpoint

Creates a geofence for AirPinpoint trackables.

## Endpoint

- **Method:** `POST`
- **Path:** `/geofences`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [Create Geofence](https://airpinpoint.com/docs/geofences)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `latitude` | body | `number` | yes |
| `longitude` | body | `number` | yes |
| `name` | body | `string` | yes |
| `notifyDestination` | body | `string` | no |
| `notifyType` | body | `string` | no |
| `radius` | body | `number` | yes |
| `trackableId[]` | body | `array<string>` | yes |
| `webhookEnabled` | body | `boolean` | no |
| `webhookSecret` | body | `string` | no |
