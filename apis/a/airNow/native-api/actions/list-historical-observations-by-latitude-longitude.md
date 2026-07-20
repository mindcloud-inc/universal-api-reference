# List Historical Observations by Latitude Longitude with AirNow

Retrieves historical air quality observations from AirNow by latitude and longitude.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/observation/latLong/historical/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Historical Observations by Latitude Longitude](https://docs.airnowapi.org/HistoricalObservationsByLatLong/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude for the requested location. |
| `longitude` | query | `number` | yes | Longitude for the requested location. |
| `date` | query | `string` | yes | Historical observation timestamp in AirNow format, for example 2026-04-08T00-0000. |
| `distance` | query | `number` | no | Search radius in miles. |
