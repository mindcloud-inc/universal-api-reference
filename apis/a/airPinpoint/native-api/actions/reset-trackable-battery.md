# Reset Trackable Battery with AirPinpoint

Resets the battery counter for a trackable in AirPinpoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/trackables/{trackableId}/battery`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [Reset Trackable Battery](https://airpinpoint.com/docs/trackables)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `batteryMonths` | body | `number` | yes |
| `trackableId` | path | `string` | yes |
