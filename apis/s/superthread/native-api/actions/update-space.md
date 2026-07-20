# Update Space with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/projects/:project_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update Space](https://superthread.com/docs/api-docs/spaces/update-a-space)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | no | Space title. |
| `project_id` | path | `string` | yes | Space ID to update. |
