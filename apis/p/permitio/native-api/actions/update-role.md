# Update Role with Permit.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/schema/:projId/:envId/roles/:roleId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Update Role](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `roleId` | path | `string` | yes | Permit role identifier. |
| `name` | body | `string` | no | Updated role display name. |
| `description` | body | `string` | no | Updated role description. |
| `permissions[]` | body | `array<string>` | no | Updated permission keys for the role. |
| `attributes` | body | `object` | no | Updated custom role attributes object. |
| `extends[]` | body | `array<string>` | no | Updated parent roles extended by this role. |
| `granted_to` | body | `object` | no | Updated granting rules object for the role. |
| `v1compat_settings` | body | `object` | no | Updated legacy v1 compatibility settings object. |
| `v1compat_attributes` | body | `object` | no | Updated legacy v1 compatibility attributes object. |
