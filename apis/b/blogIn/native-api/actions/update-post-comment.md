# Update Post Comment with BlogIn

Updates a comment on a BlogIn post.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/:postId/comments/:commentId`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Update Post Comment](https://blogin.co/api/rest/docs/#update-a-post-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postId` | path | `number` | yes | The ID of the parent post. |
| `commentId` | path | `number` | yes | The ID of the comment to update. |
| `text` | body | `string` | yes | The HTML text of the comment. |
| `author.id` | body | `number` | yes | The ID of the author of the comment. |
