# List Network Members with Mighty Networks

Retrieves members from the current Mighty Networks network.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/members`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Network Members](https://docs.mightynetworks.com/api-reference/members/return-members-of-the-given-network)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
