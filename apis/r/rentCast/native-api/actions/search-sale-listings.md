# Search Sale Listings with RentCast

Finds sale listings in RentCast by address or area.

## Endpoint

- **Method:** `GET`
- **Path:** `/listings/sale`
- **Base URL:** `https://api.rentcast.io/v1`
- **Official documentation:** [Search Sale Listings](https://developers.rentcast.io/reference/sale-listings)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | City name used to search for sale listings in a specific city. |
| `state` | query | `string` | no | Two-character state abbreviation used to search for sale listings in a specific state. |
| `address` | query | `string` | no | Full street address used to search for a specific property or a circular area when paired with radius. |
| `zipCode` | query | `string` | no | 5-digit zip code used to search for listings in a specific area. |
| `latitude` | query | `number` | no | Latitude of the circular search area when searching by coordinates. |
| `longitude` | query | `number` | no | Longitude of the circular search area when searching by coordinates. |
| `radius` | query | `number` | no | Radius in miles used with address or coordinates to search within a circular area. |
| `status` | query | `list<string>` | no | Listing status selector. RentCast documents Active and Inactive values. Accepted values: `Active`, `Inactive`. |
| `includeTotalCount` | query | `boolean` | no | When enabled, RentCast returns the total number of matching listings in the X-Total-Count response header. |
