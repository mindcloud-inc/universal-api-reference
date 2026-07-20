# Find ticket attachments with Atera

Finds attachments for a specific Atera ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tickets/:ticketId/attachments`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Find ticket attachments](https://app.atera.com/apidocs#!/Ticket/Ticket_GetAttachmentsByTicketIdAsync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | System ticket ID. |
