# Search Customers with OPN

Finds customers in OPN by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/search`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Search Customers](https://docs.omise.co/search-query-and-filters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Free-text search query. |
