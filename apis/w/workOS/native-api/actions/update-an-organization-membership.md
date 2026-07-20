# Update an organization membership with WorkOS

Updates an organization membership in your WorkOS environment.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user_management/organization_memberships/{id}`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Update an organization membership](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the organization membership. |
| `role_slug` | body | `string` | no | A single role identifier. Defaults to `member` or the explicit default role. Mutually exclusive with `role_slugs`. |
| `role_slugs` | body | `list<string>` | no | An array of role identifiers. Limited to one role when Multiple Roles is disabled. Mutually exclusive with `role_slug`. |
