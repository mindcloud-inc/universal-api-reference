# Update Task Status with Morningmate

Updates a task status in Morningmate.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/posts/projects/[:projectId]/tasks/[:taskId]/status`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Update Task Status](https://api.morningmate.com/docs/api/v1/posts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `taskId` | path | `number` | yes |
| `registerId` | body | `string` | yes |
| `status` | body | `string` | yes |
