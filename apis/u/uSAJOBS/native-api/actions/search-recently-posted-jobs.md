# Search Recently Posted Jobs with USAJOBS

Finds recently posted jobs in USAJOBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Recently Posted Jobs](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DatePosted` | query | `string` | no | Number of days posted, from 0 through 60. |
