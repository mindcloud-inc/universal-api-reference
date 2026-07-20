# Create Sprint with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/sprints`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Sprint](https://superthread.com/docs/api-docs/sprints/create-a-sprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `project_id` | body | `string` | yes | Project ID to attach the sprint to. |
| `title` | body | `string` | yes | Sprint title. |
