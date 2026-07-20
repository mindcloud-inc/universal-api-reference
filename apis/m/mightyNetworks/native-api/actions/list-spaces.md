# List Spaces with Mighty Networks

Retrieves spaces from a Mighty Networks network.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/spaces`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Spaces](https://docs.mightynetworks.com/api-reference/spaces/returns-a-list-of-spaces-for-the-current-network)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
