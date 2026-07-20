# List Ticket Filter Tickets with Deskpro

Retrieves tickets from a Deskpro ticket filter.

## Endpoint

- **Method:** `GET`
- **Path:** `/ticket_filters/:ticketFilterId/tickets`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [List Ticket Filter Tickets](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-ticket_filters-{ticketFilter}-tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketFilterId` | path | `number` | yes |
