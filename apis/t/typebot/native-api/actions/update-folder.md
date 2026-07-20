# Update Folder with Typebot

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/folders/:folderId`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Update Folder](https://docs.typebot.io/api-reference/folder/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID to update. |
| `workspaceId` | body | `string` | yes | Workspace ID that owns the folder. |
| `folder.name` | body | `string` | no | Updated folder name. |
| `folder.parentFolderId` | body | `string` | no | Updated parent folder ID. |
