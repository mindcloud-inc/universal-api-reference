# Update Workspace with Typebot

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/workspaces/:workspaceId`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Update Workspace](https://docs.typebot.io/api-reference/workspace/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID to update. |
| `name` | body | `string` | no | Updated workspace name. |
| `icon` | body | `string` | no | Updated workspace icon. |
