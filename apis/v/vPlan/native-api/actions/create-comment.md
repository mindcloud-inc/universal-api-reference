# Create Comment with vPlan

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/[:collection_id]/comment`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Create Comment](https://docs.api.vplan.com/comment.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | — |
| `text` | body | `string` | no | Comment text. |
