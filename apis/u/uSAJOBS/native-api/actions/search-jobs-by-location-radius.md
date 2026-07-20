# Search Jobs By Location Radius with USAJOBS

Finds jobs in USAJOBS within a location radius.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Jobs By Location Radius](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LocationName` | query | `string` | no | Base location used with Radius. |
| `Radius` | query | `string` | no | Radius to expand the location search. |
