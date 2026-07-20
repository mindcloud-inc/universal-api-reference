# List Space Members with Mighty Networks

Retrieves members from a space in Mighty Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/spaces/:space_id/members`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Space Members](https://docs.mightynetworks.com/api-reference/members/return-members-of-the-given-space)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `space_id` | path | `number` | yes | ID of the space. |
