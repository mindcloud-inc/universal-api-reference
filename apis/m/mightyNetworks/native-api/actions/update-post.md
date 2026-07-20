# Update Post with Mighty Networks

Updates an existing post or article in Mighty Networks.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/networks/:network_id/posts/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Update Post](https://docs.mightynetworks.com/api-reference/posts/update-an-existing-post-or-article-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | Network ID. |
| `id` | path | `number` | yes | Post ID. |
| `title` | body | `string` | no | Updated post title. |
| `description` | body | `string` | no | Updated plain-text post content. |
| `notify` | query | `boolean` | no | Notify the network about the updated post. |
