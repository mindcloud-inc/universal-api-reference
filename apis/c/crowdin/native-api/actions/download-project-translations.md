# Download Project Translations with Crowdin

Retrieves a download link for project translations in Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/translations/builds/:buildId/download`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Download Project Translations](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.download.download)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `buildId` | path | `number` | yes |
