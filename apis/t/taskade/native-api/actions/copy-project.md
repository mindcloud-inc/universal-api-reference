# Copy Project with Taskade

Copies a Taskade project into a folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/copy`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Copy Project](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/copy-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `folderId` | body | `string` | yes | Folder ID. |
| `projectTitle` | body | `string` | no | Optional title for the copied project. |
