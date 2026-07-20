# Unarchive Ticket with SupportBee

Unarchives a ticket in SupportBee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id/archive`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Unarchive Ticket](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1archive/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
