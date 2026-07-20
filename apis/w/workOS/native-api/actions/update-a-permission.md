# Update a permission with WorkOS

Updates a permission in your WorkOS environment.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/authorization/permissions/{slug}`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Update a permission](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |
| `name` | body | `string` | no | A descriptive name for the Permission. |
| `description` | body | `string` | no | An optional description of the Permission. |
| `slug` | path | `string` | yes | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |
| `name` | body | `string` | no | A descriptive name for the Permission. |
| `description` | body | `string` | no | An optional description of the Permission. |
