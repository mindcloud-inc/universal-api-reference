# Get Network Member with Mighty Networks

Retrieves a network member from Mighty Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/members/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Network Member](https://docs.mightynetworks.com/api-reference/members/return-a-single-member-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `id` | path | `number` | yes | ID of the member. |
