# Create Block Comment with Are.na

Creates a new comment on a block in Are.na.

## Endpoint

- **Method:** `POST`
- **Path:** `blocks/:id/comments`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Create Block Comment](https://www.are.na/developers/explore/block/post-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Comment body. |
| `id` | path | `string` | no | Are.na block ID. |
