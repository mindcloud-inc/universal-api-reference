# Get Space with Mighty Networks

Retrieves a space from Mighty Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/spaces/:id`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Space](https://docs.mightynetworks.com/api-reference/spaces/query-details-of-a-specific-space-by-its-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `id` | path | `number` | yes | The ID of the space to retrieve. |
