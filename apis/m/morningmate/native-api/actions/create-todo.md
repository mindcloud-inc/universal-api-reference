# Create Todo with Morningmate

Creates a todo in a Morningmate project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/projects/[:projectId]/todos`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Create Todo](https://api.morningmate.com/docs/api/v1/posts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `registerId` | body | `string` | yes |
| `title` | body | `string` | yes |
| `todoList[]` | body | `array<object>` | yes |
| `contents` | body | `string` | yes |
