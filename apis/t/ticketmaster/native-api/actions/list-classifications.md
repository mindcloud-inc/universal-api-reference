# List Classifications with Ticketmaster

Finds classifications in Ticketmaster by name and related filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery/v2/classifications`
- **Base URL:** `https://app.ticketmaster.com`
- **Official documentation:** [List Classifications](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-classifications-v2)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Keyword to search on. |
