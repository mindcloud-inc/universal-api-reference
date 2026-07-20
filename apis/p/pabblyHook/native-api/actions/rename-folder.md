# Rename Folder with Pabbly Hook

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/folders/rename/:folderId`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Rename Folder](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID from Pabbly Hook. |
| `name` | body | `string` | yes | New folder name. |
