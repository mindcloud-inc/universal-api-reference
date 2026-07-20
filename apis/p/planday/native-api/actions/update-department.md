# Update Department with Planday

Updates an existing department in Planday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/hr/v1.0/departments/:id`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Update Department](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
| `number` | body | `string` | no |
