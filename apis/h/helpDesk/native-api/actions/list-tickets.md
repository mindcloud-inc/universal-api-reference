# List Tickets with HelpDesk

Retrieves tickets from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tickets`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [List Tickets](https://api.helpdesk.com/docs#tag/Tickets/operation/ticketList)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Full-text search query for matching tickets. |
| `silo` | query | `string` | no | Ticket folder to list from, such as tickets or archive. |
| `sortBy` | query | `string` | no | Field used to sort the ticket list. |
| `order` | query | `string` | no | Sort direction for the ticket list. |
| `next.value` | query | `string` | no | Cursor timestamp from the last ticket on the current page. |
| `next.ID` | query | `string` | no | Cursor ticket ID from the last ticket on the current page. |
