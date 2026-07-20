# List Venues with Ticketmaster

Finds venues in Ticketmaster by name and related filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery/v2/venues`
- **Base URL:** `https://app.ticketmaster.com`
- **Official documentation:** [List Venues](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-venues-v2)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Keyword to search on. |
