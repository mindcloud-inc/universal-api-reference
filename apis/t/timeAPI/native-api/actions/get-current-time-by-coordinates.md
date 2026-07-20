# Get Current Time By Coordinates with TimeAPI

Retrieves the current time by coordinates from TimeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/time/current/coordinate`
- **Base URL:** `https://www.timeapi.io`
- **Official documentation:** [Get Current Time By Coordinates](https://www.timeapi.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude ranging from -90 to 90. |
| `longitude` | query | `number` | yes | Longitude ranging from -180 to 180. |
