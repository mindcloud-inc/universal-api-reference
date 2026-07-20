# List Current Observations by Latitude Longitude with AirNow

Retrieves current air quality observations from AirNow by latitude and longitude.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/observation/latLong/current/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Current Observations by Latitude Longitude](https://docs.airnowapi.org/CurrentObservationsByLatLon/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude for the requested location. |
| `longitude` | query | `number` | yes | Longitude for the requested location. |
| `distance` | query | `number` | no | Search radius in miles. |
