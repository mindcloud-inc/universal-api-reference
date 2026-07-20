# Create Post Comment with Mighty Networks

Creates a comment on a post in Mighty Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/networks/:network_id/posts/:post_id/comments`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Create Post Comment](https://docs.mightynetworks.com/api-reference/comments/create-a-new-comment-on-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `post_id` | path | `number` | yes | The ID of the post where the comment will be created. |
| `text` | body | `string` | yes | The content of the comment. |
| `reply_to_id` | body | `number` | no | The ID of the parent comment when creating a reply. |
