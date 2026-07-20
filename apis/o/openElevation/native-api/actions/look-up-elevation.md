# Look Up Elevation with Open-Elevation

Retrieves elevations from Open-Elevation for coordinates in the query string.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/lookup`
- **Base URL:** `https://api.open-elevation.com`
- **Official documentation:** [Look Up Elevation](https://github.com/Jorl17/open-elevation/blob/master/docs/api.md#get-apiv1lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locations` | query | `string` | yes | Latitude,longitude pairs separated by \|, for example 41.161758,-8.583933 or 10,10\|20,20. |
