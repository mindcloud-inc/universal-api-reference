# Create Reply with SupportBee

Creates a reply on a SupportBee ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/replies`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Create Reply](https://supportbee.com/docs/api/reference#tag/Replies/paths/~1tickets~1{id}~1replies/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
| `reply.content.text` | body | `string` | yes | Plain-text reply body. |
