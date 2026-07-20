# Build Project Translation with Crowdin

Starts a project translation build in Crowdin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/translations/builds`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Build Project Translation](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `branchId` | body | `number` | no |
| `targetLanguageIds[]` | body | `array<string>` | no |
| `skipUntranslatedStrings` | body | `boolean` | no |
| `skipUntranslatedFiles` | body | `boolean` | no |
| `exportApprovedOnly` | body | `boolean` | no |
