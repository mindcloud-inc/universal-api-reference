# List Folder Agents with Taskade

Retrieves agents from a Taskade folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/agents`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List Folder Agents](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-agents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
