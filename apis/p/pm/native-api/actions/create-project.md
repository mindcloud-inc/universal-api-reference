# Create Project with 5pm

Creates a new project in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/projects/add`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Create Project](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project[name]` | query | `string` | yes | Name of the project to create. |
