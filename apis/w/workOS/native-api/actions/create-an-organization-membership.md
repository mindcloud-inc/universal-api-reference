# Create an organization membership with WorkOS

Creates an organization membership in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_management/organization_memberships`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Create an organization membership](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | The ID of the [user](/reference/authkit/user). |
| `organization_id` | body | `string` | yes | The ID of the [organization](/reference/organization) which the user belongs to. |
| `role_slug` | body | `string` | no | A single role identifier. Defaults to `member` or the explicit default role. Mutually exclusive with `role_slugs`. |
| `role_slugs` | body | `list<string>` | no | An array of role identifiers. Limited to one role when Multiple Roles is disabled. Mutually exclusive with `role_slug`. |
