# List Sprints with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/sprints`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [List Sprints](https://superthread.com/docs/api-docs/sprints/get-sprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `team_id` | path | `string` | yes |
| `project_id` | query | `string` | yes |
| `archived` | query | `boolean` | no |
