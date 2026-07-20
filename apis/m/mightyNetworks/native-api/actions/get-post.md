# Get Post with Mighty Networks

Retrieves a post from Mighty Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/posts/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Post](https://docs.mightynetworks.com/api-reference/posts/query-details-of-a-specific-post-by-its-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | Network ID. |
| `id` | path | `number` | yes | Post ID. |
