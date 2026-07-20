# Search Tickets with Request Tracker (RT)

Finds tickets in Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `tickets`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Search Tickets](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated RT fields to include in each ticket result. |
| `query` | query | `string` | yes | TicketSQL query to search RT tickets. |
| `search` | query | `string` | no | Saved search ID or description to run. Query takes precedence when both are set. |
| `simple` | query | `boolean` | no | Set to true to use RT simple search syntax instead of TicketSQL. |
