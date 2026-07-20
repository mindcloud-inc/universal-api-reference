# Create a permission with WorkOS

Creates a permission in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/authorization/permissions`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Create a permission](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | body | `string` | yes | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |
| `name` | body | `string` | yes | A descriptive name for the Permission. |
| `description` | body | `string` | no | An optional description of the Permission. |
| `resource_type_slug` | body | `string` | no | The slug of the resource type this permission is scoped to. |
| `slug` | body | `string` | yes | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |
| `name` | body | `string` | yes | A descriptive name for the Permission. |
| `description` | body | `string` | no | An optional description of the Permission. |
| `resource_type_slug` | body | `string` | no | The slug of the resource type this permission is scoped to. |
