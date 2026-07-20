# Update Resource with Permit.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/schema/:projId/:envId/resources/:resourceId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Update Resource](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `resourceId` | path | `string` | yes | Permit resource identifier. |
| `name` | body | `string` | no | Updated resource display name. |
| `urn` | body | `string` | no | Updated resource URN. |
| `description` | body | `string` | no | Updated resource description. |
| `actions` | body | `object` | no | Updated actions definition object for the resource. |
| `type_attributes` | body | `object` | no | Updated type attributes object for the resource. |
| `attributes` | body | `object` | no | Updated custom resource attributes object. |
| `roles` | body | `object` | no | Updated roles definition object for the resource. |
| `relations` | body | `object` | no | Updated relations definition object for the resource. |
| `v1compat_path` | body | `string` | no | Updated legacy v1 compatibility path. |
| `v1compat_type` | body | `string` | no | Updated legacy v1 compatibility type. |
| `v1compat_name` | body | `string` | no | Updated legacy v1 compatibility name. |
