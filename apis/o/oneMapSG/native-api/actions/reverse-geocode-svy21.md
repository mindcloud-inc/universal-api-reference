# Reverse Geocode (SVY21 Coordinates) with OneMap SG

Retrieves an address from OneMap SG by SVY21 coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/revgeocodexy`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Reverse Geocode (SVY21 Coordinates)](https://www.onemap.gov.sg/apidocs/reversegeocode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | yes | SVY21 X and Y coordinates as a comma-separated pair. |
| `buffer` | query | `number` | no | The search buffer around the location. |
| `addressType` | query | `string` | no | The address type to include in the reverse geocode response. |
