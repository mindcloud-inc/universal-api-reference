# List Project Tasks with Crowdin

Retrieves project tasks from Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [List Project Tasks](https://support.crowdin.com/developer/api/v2/#operation/api.projects.tasks.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `orderBy` | query | `string` | no |
| `status` | query | `string` | no |
| `assigneeId` | query | `number` | no |
