# List Plans with Mighty Networks

Retrieves plans from a Mighty Networks network.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/plans`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Plans](https://docs.mightynetworks.com/api-reference/plans/return-all-plans-in-the-network)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
