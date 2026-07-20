# Move Ticket with Zoho Desk

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/[:ticketId]/move`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Move Ticket](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The Zoho Desk ticket ID. |
| `departmentId` | body | `string` | yes | Target department for the ticket move. |
