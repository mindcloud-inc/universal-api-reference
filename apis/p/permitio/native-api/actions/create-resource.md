# Create Resource with Permit.io

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/schema/:projId/:envId/resources`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Create Resource](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `key` | body | `string` | yes | Unique resource key within the Permit environment. |
| `name` | body | `string` | yes | Resource display name. |
| `urn` | body | `string` | no | Resource URN. |
| `description` | body | `string` | no | Resource description. |
| `actions` | body | `object` | yes | Actions definition object for the resource. |
| `type_attributes` | body | `object` | no | Type attributes object for the resource. |
| `attributes` | body | `object` | no | Custom resource attributes object. |
| `roles` | body | `object` | no | Roles definition object for the resource. |
| `relations` | body | `object` | no | Relations definition object for the resource. |
| `v1compat_path` | body | `string` | no | Legacy v1 compatibility path. |
| `v1compat_type` | body | `string` | no | Legacy v1 compatibility type. |
| `v1compat_name` | body | `string` | no | Legacy v1 compatibility name. |
