# Delete Post with Mighty Networks

Deletes an existing post or article from Mighty Networks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/networks/:network_id/posts/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Delete Post](https://docs.mightynetworks.com/api-reference/posts/delete-a-post-or-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID. |
| `id` | path | `number` | yes | The ID of the post to delete. |
