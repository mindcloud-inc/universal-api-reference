# Get Placekeys with Placekey

Retrieves Placekeys for multiple locations in Placekey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/placekeys`
- **Base URL:** `https://api.placekey.io`
- **Official documentation:** [Get Placekeys](https://docs.placekey.io/documentation/placekey-api/bulk-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queries[].queryId` | body | `string` | no | Optional ID echoed back in the response for this query. |
| `queries[].locationName` | body | `string` | no | Name of the point of interest to match, when available. |
| `queries[].streetAddress` | body | `string` | no | Street address of the place. |
| `queries[].city` | body | `string` | no | City where the place is located. |
| `queries[].region` | body | `string` | no | Second-level administrative region, such as a US state. |
| `queries[].postalCode` | body | `string` | no | Postal code of the place. |
| `queries[].isoCountryCode` | body | `string` | no | ISO 2-letter country code. Placekey requires all queries in a batch to use the same iso_country_code when supplied. |
| `queries[].latitude` | body | `number` | no | Latitude in WGS-84 coordinates. |
| `queries[].longitude` | body | `number` | no | Longitude in WGS-84 coordinates. |
