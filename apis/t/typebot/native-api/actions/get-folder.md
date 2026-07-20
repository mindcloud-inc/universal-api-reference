# Get Folder with Typebot

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/folders/:folderId`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Get Folder](https://docs.typebot.io/api-reference/folder/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID to retrieve. |
| `workspaceId` | query | `string` | yes | Workspace ID that owns the folder. |
