# Search Companies with CATS

Finds companies in CATS by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/search`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Search Companies](https://docs.catsone.com/api/v3/#companies-search-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The string to search within companies for. |
