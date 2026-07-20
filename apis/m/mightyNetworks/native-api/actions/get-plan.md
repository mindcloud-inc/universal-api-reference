# Get Plan with Mighty Networks

Retrieves a plan from Mighty Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/plans/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Plan](https://docs.mightynetworks.com/api-reference/plans/return-a-single-plan-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `id` | path | `number` | yes | The ID of the plan to retrieve. |
