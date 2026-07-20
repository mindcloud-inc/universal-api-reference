# Archive Project with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/epics/:epic_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Archive Project](https://superthread.com/docs/api-docs/projects/archive-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `epic_id` | path | `string` | yes | Project ID to archive. |
