# Update Comment with Nozbe Personal

Updates an existing comment in Nozbe Personal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Comment](https://api4.nozbe.com/v1/api#/comments/putCommentById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Comment ID to update. |
| `body` | body | `string` | no | Updated comment body. |
