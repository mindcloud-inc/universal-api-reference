# Get Time Zone Details By Coordinates with TimeAPI

Retrieves time zone details by coordinates from TimeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/timezone/coordinate`
- **Base URL:** `https://www.timeapi.io`
- **Official documentation:** [Get Time Zone Details By Coordinates](https://www.timeapi.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude for timezone lookup. |
| `longitude` | query | `number` | yes | Longitude for timezone lookup. |
