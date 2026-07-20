# List Current Observations by Zip Code with AirNow

Retrieves current air quality observations from AirNow by zip code.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/observation/zipCode/current/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Current Observations by Zip Code](https://docs.airnowapi.org/CurrentObservationsByZip/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zipCode` | query | `string` | yes | The zip code used to resolve the reporting area. |
| `distance` | query | `number` | no | Search radius in miles when no direct reporting-area match exists. |
