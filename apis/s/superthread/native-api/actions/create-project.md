# Create Project with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/epics`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Project](https://superthread.com/docs/api-docs/projects/create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `list_id` | body | `string` | yes | Workflow list to attach the project to. |
| `title` | body | `string` | yes | Project title. |
