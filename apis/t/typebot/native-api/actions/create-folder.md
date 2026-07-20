# Create Folder with Typebot

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/folders`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Create Folder](https://docs.typebot.io/api-reference/folder/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | Workspace ID to create the folder in. |
| `folderName` | body | `string` | no | Optional folder name. |
| `parentFolderId` | body | `string` | no | Optional parent folder ID. |
