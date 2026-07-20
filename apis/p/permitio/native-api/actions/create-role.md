# Create Role with Permit.io

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/schema/:projId/:envId/roles`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Create Role](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `key` | body | `string` | yes | Unique role key within the Permit environment. |
| `name` | body | `string` | yes | Role display name. |
| `description` | body | `string` | no | Role description. |
| `permissions[]` | body | `array<string>` | no | Permission keys granted to the role. |
| `attributes` | body | `object` | no | Custom role attributes object. |
| `extends[]` | body | `array<string>` | no | Parent roles extended by this role. |
| `granted_to` | body | `object` | no | Granting rules object for the role. |
| `v1compat_settings` | body | `object` | no | Legacy v1 compatibility settings object. |
| `v1compat_attributes` | body | `object` | no | Legacy v1 compatibility attributes object. |
| `v1compat_is_built_in` | body | `boolean` | no | Marks the role as built in for legacy compatibility. |
