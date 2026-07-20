# Get Stops For Location with BKK Futar

Retrieves stops for a selected location, or all stops, in BKK Futar.

## Endpoint

- **Method:** `GET`
- **Path:** `/stops-for-location.json`
- **Base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`
- **Official documentation:** [Get Stops For Location](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-stops-for-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | no | Latitude of the requested location. |
| `lon` | query | `number` | no | Longitude of the requested location. |
| `latSpan` | query | `number` | no | Latitude span around the requested location. |
| `lonSpan` | query | `number` | no | Longitude span around the requested location. |
| `radius` | query | `number` | no | Search radius in meters when spans are omitted. |
| `minResult` | query | `number` | no | Minimum number of elements returned. |
| `includeReferences` | query | `string` | no | Reference data to include in the response. |
