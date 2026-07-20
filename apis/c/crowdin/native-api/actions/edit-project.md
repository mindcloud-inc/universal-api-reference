# Edit Project with Crowdin

Updates an existing project in Crowdin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Edit Project](https://support.crowdin.com/developer/api/v2/#operation/api.projects.patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `operations[]` | body | `array<object>` | yes |
