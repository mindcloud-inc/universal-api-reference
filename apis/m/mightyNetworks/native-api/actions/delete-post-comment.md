# Delete Post Comment with Mighty Networks

Deletes a comment from a post in Mighty Networks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/networks/:network_id/posts/:post_id/comments/:id`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Delete Post Comment](https://docs.mightynetworks.com/api-reference/comments/delete-a-comment-from-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `post_id` | path | `number` | yes | The ID of the post that owns the comment. |
| `id` | path | `number` | yes | The ID of the comment to delete. |
