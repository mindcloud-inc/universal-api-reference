# List Tags on a Ticket with Zoho Desk

This API lists tags associated with a ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId/tags`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [List Tags on a Ticket](https://desk.zoho.com/DeskAPIDocument#TicketTags#TicketTags_Listtickettags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | ID of a ticket for which tags will be fetched. |
