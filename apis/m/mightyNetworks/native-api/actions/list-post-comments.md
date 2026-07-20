# List Post Comments with Mighty Networks

Retrieves comments for a Mighty Networks post.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/posts/:post_id/comments`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Post Comments](https://docs.mightynetworks.com/api-reference/comments/returns-a-list-of-comments-for-a-specific-post)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `post_id` | path | `number` | yes | The ID of the post whose comments you want to list. |
