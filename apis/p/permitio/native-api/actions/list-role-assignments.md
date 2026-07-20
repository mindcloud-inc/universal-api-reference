# List Role Assignments with Permit.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/facts/:projId/:envId/role_assignments`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [List Role Assignments](https://api.permit.io/scalar)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
