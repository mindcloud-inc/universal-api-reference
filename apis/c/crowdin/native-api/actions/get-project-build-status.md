# Get Project Build Status with Crowdin

Retrieves project build status from Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/translations/builds/:buildId`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Get Project Build Status](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `buildId` | path | `number` | yes |
