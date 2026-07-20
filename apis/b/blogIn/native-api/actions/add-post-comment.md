# Add Post Comment with BlogIn

Adds a comment to a BlogIn post.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/:id/comments`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Add Post Comment](https://blogin.co/api/rest/docs/#create-new-post-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the post to comment on. |
| `text` | body | `string` | yes | The HTML text of the comment. |
| `author.id` | body | `number` | yes | The ID of the author of the comment. |
