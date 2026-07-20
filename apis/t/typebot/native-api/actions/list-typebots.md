# List Typebots with Typebot

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/typebots`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [List Typebots](https://docs.typebot.io/api-reference/typebot/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | yes | Workspace ID to list typebots from. |
| `folderId` | query | `string` | no | Optional folder ID to filter typebots. |
