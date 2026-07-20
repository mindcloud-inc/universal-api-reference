# List Historical Observations by Zip Code with AirNow

Retrieves historical air quality observations from AirNow by zip code.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/observation/zipCode/historical/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Historical Observations by Zip Code](https://docs.airnowapi.org/HistoricalObservationsByZip/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zipCode` | query | `string` | yes | The zip code used to resolve the reporting area. |
| `date` | query | `string` | yes | Historical observation timestamp in AirNow format, for example 2026-04-08T00-0000. |
| `distance` | query | `number` | no | Search radius in miles. |
