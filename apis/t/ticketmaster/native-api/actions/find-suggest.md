# Find Suggest with Ticketmaster

Finds search suggestions in Ticketmaster by keyword and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery/v2/suggest.json`
- **Base URL:** `https://app.ticketmaster.com`
- **Official documentation:** [Find Suggest](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#finding-events-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Keyword to search on. |
| `size` | query | `number` | no | Maximum number of suggestion results to return. Ticketmaster allows 1 to 5 for this endpoint. |
