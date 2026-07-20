# Add File with Crowdin

Creates a new file in a Crowdin project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/files`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Add File](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `storageId` | body | `number` | yes |
| `name` | body | `string` | yes |
| `branchId` | body | `number` | no |
| `directoryId` | body | `number` | no |
| `title` | body | `string` | no |
| `context` | body | `string` | no |
| `type` | body | `string` | no |
| `parserVersion` | body | `number` | no |
| `importOptions` | body | `object` | no |
| `exportOptions` | body | `object` | no |
| `excludedTargetLanguages[]` | body | `array<string>` | no |
| `attachLabelIds[]` | body | `array<number>` | no |
