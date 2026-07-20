# Create Task with Morningmate

Creates a task in a Morningmate project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/projects/[:projectId]/tasks`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Create Task](https://api.morningmate.com/docs/api/v1/posts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `registerId` | body | `string` | yes |
| `title` | body | `string` | yes |
| `contents` | body | `string` | yes |
| `status` | body | `string` | yes |
