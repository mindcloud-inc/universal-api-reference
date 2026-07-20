# Get Placekey with Placekey

Retrieves a Placekey for one location in Placekey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/placekey`
- **Base URL:** `https://api.placekey.io`
- **Official documentation:** [Get Placekey](https://docs.placekey.io/documentation/placekey-api/quick-start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query.locationName` | body | `string` | no | Name of the point of interest to match, when available. |
| `query.streetAddress` | body | `string` | no | Street address of the place. |
| `query.city` | body | `string` | no | City where the place is located. |
| `query.region` | body | `string` | no | Second-level administrative region, such as a US state. |
| `query.postalCode` | body | `string` | no | Postal code of the place. |
| `query.isoCountryCode` | body | `string` | no | ISO 2-letter country code for the place. |
| `query.latitude` | body | `number` | no | Latitude in WGS-84 coordinates. |
| `query.longitude` | body | `number` | no | Longitude in WGS-84 coordinates. |
| `options.fields` | body | `list<string>` | no | Optional response fields to request, such as address_placekey, building_placekey, confidence_score, normalized_address, geocode, upi, geoid, parcel, or gers. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. Send multiple values as a array. |
