# Update Folder with MetaSurvey

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/folder/:folderId`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder to update. |
| `name` | body | `string` | yes | Updated folder name. |
