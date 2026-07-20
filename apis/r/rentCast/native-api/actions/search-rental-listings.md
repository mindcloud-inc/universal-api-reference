# Search Rental Listings with RentCast

Finds rental listings in RentCast by address or area.

## Endpoint

- **Method:** `GET`
- **Path:** `/listings/rental/long-term`
- **Base URL:** `https://api.rentcast.io/v1`
- **Official documentation:** [Search Rental Listings](https://developers.rentcast.io/reference/rental-listings-long-term)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | The city to search for rental listings in. |
| `state` | query | `string` | no | The 2-letter state abbreviation used with city to search for rental listings. |
| `address` | query | `string` | no | A full street address, optionally combined with radius to search nearby rental listings. |
| `zipCode` | query | `string` | no | The 5-digit zip code used to search for rental listings in a specific area. |
| `latitude` | query | `number` | no | Latitude of the circular search area when searching by coordinates. |
| `longitude` | query | `number` | no | Longitude of the circular search area when searching by coordinates. |
| `radius` | query | `number` | no | Radius in miles used with address or coordinates to search within a circular area. |
| `status` | query | `list<string>` | no | The listing status to match. Accepted values: `Active`, `Inactive`. |
| `includeTotalCount` | query | `boolean` | no | When enabled, RentCast returns the total number of matching rental listings in the X-Total-Count response header. |
