# List Roles with Permit.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/schema/:projId/:envId/roles`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [List Roles](https://api.permit.io/scalar)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
