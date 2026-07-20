# List Posts with Mighty Networks

Retrieves posts from a Mighty Networks network.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/posts`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Posts](https://docs.mightynetworks.com/api-reference/posts/returns-a-list-of-posts-for-the-current-network)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | Network ID. |
| `space_id` | query | `number` | no | Return only posts from a specific space. |
