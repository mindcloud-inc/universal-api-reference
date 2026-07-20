# Generate Agent in Folder with Taskade

Generates a Taskade agent from text in a folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folderId/agent-generate`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Generate Agent in Folder](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/generate-agent-in-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder identifier from the path. |
| `text` | body | `string` | yes | Prompt used to generate the agent. |
