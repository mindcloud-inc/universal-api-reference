# Trash Ticket with SupportBee

Moves a SupportBee ticket to trash.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/trash`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Trash Ticket](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1trash/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
