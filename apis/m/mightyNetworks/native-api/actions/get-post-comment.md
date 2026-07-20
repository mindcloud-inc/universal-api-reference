# Get Post Comment with Mighty Networks

Retrieves a comment from a Mighty Networks post.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/posts/:post_id/comments/:id`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Post Comment](https://docs.mightynetworks.com/api-reference/comments/query-details-of-a-specific-comment-by-its-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `network_id` | path | `string` | yes |
| `post_id` | path | `number` | yes |
| `id` | path | `number` | yes |
