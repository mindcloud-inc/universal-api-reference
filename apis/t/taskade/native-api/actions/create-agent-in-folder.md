# Create Agent in Folder with Taskade

Creates a new Taskade agent in a folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folderId/agents`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Create Agent in Folder](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/create-agent-in-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder identifier from the path. |
| `name` | body | `string` | yes | Agent name. |
| `data.data.commands[].name` | body | `string` | yes | Single command display name. |
| `data.data.commands[].prompt` | body | `string` | yes | Single command prompt text. |
| `data.data.description` | body | `string` | yes | Agent description. |
| `data.data.avatar.data.value` | body | `string` | yes | Avatar emoji value. |
