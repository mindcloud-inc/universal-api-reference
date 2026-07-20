# Delete Ticket with Zammad

Deletes an existing ticket from Zammad.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:ticketId`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Delete Ticket](https://docs.zammad.org/en/latest/api/ticket/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | Ticket identifier. |
