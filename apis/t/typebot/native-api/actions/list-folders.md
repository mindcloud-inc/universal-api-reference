# List Folders with Typebot

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/folders`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [List Folders](https://docs.typebot.io/api-reference/folder/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | yes | Workspace ID to list folders from. |
| `parentFolderId` | query | `string` | no | Optional parent folder ID filter. |
