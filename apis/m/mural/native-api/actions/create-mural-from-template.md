# Create Mural from Template with Mural

Creates a new mural in Mural from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:templateId/murals`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Create Mural from Template](https://developers.mural.co/public/reference/createmuralfromtemplate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | path | `string` | yes |
| `roomId` | body | `number` | yes |
| `title` | body | `string` | yes |
| `folderId` | body | `string` | no |
