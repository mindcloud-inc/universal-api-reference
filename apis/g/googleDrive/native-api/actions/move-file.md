# Move File with Google Drive

Move a File to a Folder.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/drive/v3/files/:fileId`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Move File](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addParents` | query | `string` | yes | Comma-separated parent folder IDs to add. For single-folder move, pass the destination folder ID. |
| `removeParents` | query | `string` | no | Comma-separated parent folder IDs to remove. Optional when only adding a parent. |
| `fileId` | path | `string` | yes | Specify the 'fileId' of a File to move. Select a File in the list or use "Search Files & Folders" to get another File in your Drive. |
