# Reverse Geocode (Latitude and Longitude) with OneMap SG

Retrieves an address from OneMap SG by latitude and longitude.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/revgeocode`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Reverse Geocode (Latitude and Longitude)](https://www.onemap.gov.sg/apidocs/reversegeocode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | yes | Latitude and longitude as a comma-separated pair. |
| `buffer` | query | `number` | no | The search buffer around the location. |
| `addressType` | query | `string` | no | The address type to include in the reverse geocode response. |
