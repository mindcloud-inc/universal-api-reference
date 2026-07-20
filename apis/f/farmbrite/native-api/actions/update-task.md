# Update task with Farmbrite

Updates an existing task in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:task_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update task](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_id` | path | `string` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
