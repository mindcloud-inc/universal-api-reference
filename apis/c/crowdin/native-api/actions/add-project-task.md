# Add Project Task with Crowdin

Creates a new project task in Crowdin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/tasks`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Add Project Task](https://support.crowdin.com/developer/api/v2/#operation/api.projects.tasks.post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `title` | body | `string` | yes |
| `languageId` | body | `string` | yes |
| `type` | body | `number` | yes |
| `fileIds[]` | body | `array<number>` | no |
| `branchIds[]` | body | `array<number>` | no |
| `status` | body | `string` | no |
| `description` | body | `string` | no |
| `splitContent` | body | `boolean` | no |
| `skipAssignedStrings` | body | `boolean` | no |
| `deadline` | body | `date` | no |
| `startedAt` | body | `date` | no |
