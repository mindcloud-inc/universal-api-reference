# Create Post with Mighty Networks

Creates a new post in Mighty Networks with optional notifications.

## Endpoint

- **Method:** `POST`
- **Path:** `/networks/:network_id/posts`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Create Post](https://docs.mightynetworks.com/api-reference/posts/create-a-new-post-and-optionally-notify-the-network)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | Network ID. |
| `space_id` | body | `number` | yes | Space that will contain the new post. |
| `title` | body | `string` | yes | Post title. |
| `description` | body | `string` | no | Plain-text post content. |
| `post_type` | body | `string` | no | Type of post to create, for example article. |
| `notify` | query | `boolean` | no | Notify the network about the new post. |
