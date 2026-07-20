# Get Ticket Message with Deskpro

Retrieves a ticket message from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId/messages/:messageId`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [Get Ticket Message](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-messages-{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | The Deskpro ticket id containing the message. |
| `messageId` | path | `number` | yes | The Deskpro ticket message id to retrieve. |
