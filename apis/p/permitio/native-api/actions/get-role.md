# Get Role with Permit.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/schema/:projId/:envId/roles/:roleId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Get Role](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `roleId` | path | `string` | yes | Permit role identifier. |
