# Create Comment with SupportBee

Creates a comment on a SupportBee ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/comments`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Create Comment](https://supportbee.com/docs/api/reference#tag/Comments/paths/~1tickets~1{id}~1comments/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
| `comment.content.text` | body | `string` | yes | Plain-text internal comment body. |
