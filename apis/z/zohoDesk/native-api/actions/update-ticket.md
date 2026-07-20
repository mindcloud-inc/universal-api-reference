# Update Ticket with Zoho Desk

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tickets/[:ticketId]`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Update Ticket](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The Zoho Desk ticket ID. |
| `subject` | body | `string` | no | Updated subject for the ticket. |
