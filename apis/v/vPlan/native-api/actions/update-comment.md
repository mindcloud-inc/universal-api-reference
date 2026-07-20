# Update Comment with vPlan

## Endpoint

- **Method:** `PUT`
- **Path:** `/collection/[:collection_id]/comment/[:comment_id]`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Update Comment](https://docs.api.vplan.com/comment.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | — |
| `comment_id` | path | `string` | yes | Comment identifier. |
| `text` | body | `string` | no | Updated comment text. |
