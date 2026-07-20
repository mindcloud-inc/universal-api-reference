# Get Ticket Log with Deskpro

Retrieves a ticket log from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId/logs/:logId`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [Get Ticket Log](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-logs-{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | The Deskpro ticket id containing the log entry. |
| `logId` | path | `number` | yes | The Deskpro ticket log id to retrieve. |
