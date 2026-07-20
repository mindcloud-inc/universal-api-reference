# Create Ticket Comment with Zoho Desk

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/[:ticketId]/comments`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Create Ticket Comment](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/TicketComment.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The Zoho Desk ticket ID. |
| `content` | body | `string` | yes | Plain-text comment content to append to the ticket. |
