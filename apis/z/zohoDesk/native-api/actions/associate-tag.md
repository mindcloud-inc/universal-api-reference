# Associate Tag with Zoho Desk

This API adds a single tag or multiple tags to a ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticketId/associateTag`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Associate Tag](https://desk.zoho.com/DeskAPIDocument#TicketTags#TicketTags_Getticketcountbytag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The ID of a Ticket you want to associate these tag(s) to. |
| `tags` | body | `string` | yes | Name(s) of the tag(s) to associate with the ticket Send multiple values as a array. |
