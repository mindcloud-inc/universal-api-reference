# Create Space with Mighty Networks

Creates a new space in Mighty Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/networks/:network_id/spaces`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Create Space](https://docs.mightynetworks.com/api-reference/spaces/create-a-new-space-in-the-network)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `name` | body | `string` | yes | The name for the new space. |
