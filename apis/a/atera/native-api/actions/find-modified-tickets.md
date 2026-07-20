# Find modified tickets with Atera

Finds recently modified tickets in Atera.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tickets/lastmodified`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Find modified tickets](https://app.atera.com/apidocs#!/Ticket/Ticket_GetTicketsByLastModifiedAsync)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Return tickets modified since this UTC timestamp. |
| `includeComments` | query | `boolean` | no | Include the ticket's last comments. |
| `includeRelations` | query | `boolean` | no | Include ticket relation information. |
