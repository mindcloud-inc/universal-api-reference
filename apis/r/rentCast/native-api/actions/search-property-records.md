# Search Property Records with RentCast

Finds property records in RentCast by address or area.

## Endpoint

- **Method:** `GET`
- **Path:** `/properties`
- **Base URL:** `https://api.rentcast.io/v1`
- **Official documentation:** [Search Property Records](https://developers.rentcast.io/reference/property-records)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | City name used to search for property records in a specific city. |
| `state` | query | `string` | no | Two-character state abbreviation used to search for property records in a specific state. |
| `address` | query | `string` | no | Full street address used to search for a specific property or a circular area when paired with radius. |
| `zipCode` | query | `string` | no | 5-digit zip code used to search for property records in a specific area. |
| `latitude` | query | `number` | no | Latitude of the circular search area when searching by coordinates. |
| `longitude` | query | `number` | no | Longitude of the circular search area when searching by coordinates. |
| `radius` | query | `number` | no | Radius in miles used with address or coordinates to search within a circular area. |
| `includeTotalCount` | query | `boolean` | no | When enabled, RentCast returns the total number of matching property records in the X-Total-Count response header. |
