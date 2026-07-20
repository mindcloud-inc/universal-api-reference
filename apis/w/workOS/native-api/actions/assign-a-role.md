# Assign a role with WorkOS

Assigns a role in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/authorization/organization_memberships/{organization_membership_id}/role_assignments`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Assign a role](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_membership_id` | path | `string` | yes | The ID of the organization membership. |
| `role_slug` | body | `string` | yes | The slug of the role to assign. |
| `resource_id` | body | `string` | no | The ID of the resource. Use either this or `resource_external_id` and `resource_type_slug`. |
| `resource_external_id` | body | `string` | no | The external ID of the resource. Requires `resource_type_slug`. |
| `resource_type_slug` | body | `string` | no | The resource type slug. Required with `resource_external_id`. |
