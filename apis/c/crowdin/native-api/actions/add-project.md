# Add Project with Crowdin

Creates a new project in Crowdin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Add Project](https://support.crowdin.com/developer/api/v2/#operation/api.projects.post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `sourceLanguageId` | body | `string` | yes | — |
| `targetLanguageIds[]` | body | `array<string>` | no | — |
| `visibility` | body | `string` | no | — |
| `languageAccessPolicy` | body | `string` | no | Defines access to project languages. Use `open` when the current Crowdin plan does not support moderated language membership. |
| `description` | body | `string` | no | — |
| `identifier` | body | `string` | no | — |
