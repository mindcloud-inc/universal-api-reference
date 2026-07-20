# Find ticket comments with Atera

Finds comments for a specific Atera ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tickets/:ticketId/comments`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Find ticket comments](https://app.atera.com/apidocs#!/Ticket/Ticket_GetComments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | System ticket ID. |
