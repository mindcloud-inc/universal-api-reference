# Create Project in Workspace with Taskade

Creates a new Taskade project in a workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/projects`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Create Project in Workspace](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/workspaces/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID. |
| `content` | body | `string` | yes | Markdown content for the new project. |
