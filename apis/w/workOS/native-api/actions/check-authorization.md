# Check authorization with WorkOS

Checks authorization in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/authorization/organization_memberships/{organization_membership_id}/check`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Check authorization](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_membership_id` | path | `string` | yes | The ID of the organization membership to check. |
| `permission_slug` | body | `string` | yes | The slug of the permission to check. |
| `resource_id` | body | `string` | no | The ID of the resource. |
| `resource_external_id` | body | `string` | no | The external ID of the resource. |
| `resource_type_slug` | body | `string` | no | The slug of the resource type. |
