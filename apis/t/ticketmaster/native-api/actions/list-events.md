# List Events with Ticketmaster

Finds events in Ticketmaster by location, date, and availability.

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery/v2/events`
- **Base URL:** `https://app.ticketmaster.com`
- **Official documentation:** [List Events](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#overview)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Keyword to search on. |
