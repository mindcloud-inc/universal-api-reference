# Restore Ticket with SupportBee

Restores a trashed SupportBee ticket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id/trash`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Restore Ticket](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1trash/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
