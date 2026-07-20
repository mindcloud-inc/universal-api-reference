# Update Project with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/epics/:epic_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update Project](https://superthread.com/docs/api-docs/projects/update-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | no | Project title. |
| `epic_id` | path | `string` | yes | Project ID to update. |
