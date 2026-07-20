# Create Workspace with Typebot

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workspaces`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Create Workspace](https://docs.typebot.io/api-reference/workspace/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Workspace name. |
| `icon` | body | `string` | no | Optional workspace icon. |
