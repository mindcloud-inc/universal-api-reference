# Look Up Elevations From Body with Open-Elevation

Retrieves elevations from Open-Elevation for coordinates in the request body.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/lookup`
- **Base URL:** `https://api.open-elevation.com`
- **Official documentation:** [Look Up Elevations From Body](https://github.com/Jorl17/open-elevation/blob/master/docs/api.md#post-apiv1lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locations[]` | body | `array<object>` | yes | Array of location objects. Each object must include latitude and longitude. |
| `locations[].latitude` | body | `number` | yes | Latitude for each location in WGS84 decimal degrees. |
| `locations[].longitude` | body | `number` | yes | Longitude for each location in WGS84 decimal degrees. |
