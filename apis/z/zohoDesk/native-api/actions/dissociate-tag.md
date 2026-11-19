# Dissociate Tag with Zoho Desk

This API removes a single tag or multiple tags from a ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticketId/dissociateTag`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Dissociate Tag](https://desk.zoho.com/DeskAPIDocument#TicketTags_DissociateTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The ID of a Ticket you want to associate these tag(s) to. |
| `tags` | body | `string` | yes | Name(s) of the tag(s) to associate with the ticket Send multiple values as a array. |
