# Create Project with Taskade

Creates a new Taskade project in a folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Create Project](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | body | `string` | yes | Folder ID. |
| `content` | body | `string` | yes | Markdown content for the new project. |
