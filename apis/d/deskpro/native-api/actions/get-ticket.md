# Get Ticket with Deskpro

Retrieves a ticket record from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [Get Ticket](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | The Deskpro ticket id to retrieve. |
