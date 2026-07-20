# Search Jobs By Location with USAJOBS

Finds jobs in USAJOBS by location.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Jobs By Location](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LocationName` | query | `string` | no | City, military installation, state, or ZIP-style location text. |
