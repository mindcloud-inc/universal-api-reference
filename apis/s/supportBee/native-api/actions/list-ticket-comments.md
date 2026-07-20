# List Ticket Comments with SupportBee

Retrieves comments for a SupportBee ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:id/comments`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [List Ticket Comments](https://supportbee.com/docs/api/reference#tag/Comments/paths/~1tickets~1{id}~1comments/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
