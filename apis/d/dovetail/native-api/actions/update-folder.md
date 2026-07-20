# Update Folder with Dovetail

Updates an existing folder in Dovetail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/folders/:folderId`
- **Base URL:** `https://dovetail.com/api`
- **Official documentation:** [Update Folder](https://developers.dovetail.com/reference/patch_v1-folders-folderid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | — |
| `title` | body | `string` | yes | Folder title. |
