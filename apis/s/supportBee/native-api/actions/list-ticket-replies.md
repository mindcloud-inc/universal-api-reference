# List Ticket Replies with SupportBee

Retrieves replies for a SupportBee ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:id/replies`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [List Ticket Replies](https://supportbee.com/docs/api/reference#tag/Replies/paths/~1tickets~1{id}~1replies/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
