# Update Folder with Canva

Updates an existing folder in Canva.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/folders/:folderId`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Update Folder](https://www.canva.dev/docs/connect/api-reference/folders/update-folder/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Maximum length: 50. |
| `name` | body | `string` | yes | Maximum length: 255. |
