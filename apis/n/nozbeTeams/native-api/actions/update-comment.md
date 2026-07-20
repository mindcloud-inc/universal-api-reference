# Update Comment with Nozbe Teams

Updates an existing comment in Nozbe Teams.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Comment](https://api4.nozbe.com/v1/api#/comments/putCommentById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The comment to update. |
| `body` | body | `string` | no | The updated comment text. |
