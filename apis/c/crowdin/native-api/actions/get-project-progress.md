# Get Project Progress with Crowdin

Retrieves project progress by language from Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/languages/progress`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Get Project Progress](https://support.crowdin.com/developer/api/v2/#operation/api.projects.languages.progress.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `languageIds[]` | query | `array<string>` | no |
