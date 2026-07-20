# Update Feedback Comment with Userback

Updates a Userback feedback comment.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/feedback/comment/:id`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Update Feedback Comment](https://docs.userback.io/reference/updatefeedbackcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feedback comment ID to update. |
| `comment` | body | `string` | no | Updated comment text. |
| `isPublic` | body | `boolean` | no | Whether the comment is public. |
| `userId` | body | `number` | no | User ID associated with the comment update. |
