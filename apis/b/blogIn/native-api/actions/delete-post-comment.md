# Delete Post Comment with BlogIn

Deletes a comment from a BlogIn post.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/posts/:postId/comments/:commentId`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Delete Post Comment](https://blogin.co/api/rest/docs/#delete-a-post-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postId` | path | `number` | yes | The ID of the parent post. |
| `commentId` | path | `number` | yes | The ID of the comment to delete. |
