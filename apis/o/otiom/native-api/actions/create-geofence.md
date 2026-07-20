# Create Geofence with Otiom

Creates a new geofence in Otiom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/geofences/`
- **Base URL:** `https://api.otiom.com`
- **Official documentation:** [Create Geofence](https://api.otiom.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `points` | body | `object` | yes | Polygon coordinates as an array of three to seven [longitude, latitude] pairs. |
| `patient` | body | `number` | no | — |
