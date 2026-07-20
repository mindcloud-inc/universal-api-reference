# Update Task with Dart

Updates an existing task in Dart.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [Update Task](https://app.dartai.com/api/v0/public/docs/#/Task/updateTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `item.description` | body | `string` | no |
| `item.id` | body | `string` | no |
| `item.status` | body | `string` | no |
| `item.title` | body | `string` | no |
