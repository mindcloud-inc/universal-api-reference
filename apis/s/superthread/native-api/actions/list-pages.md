# List Pages with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/pages`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [List Pages](https://superthread.com/docs/api-docs/pages/get-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Include archived pages when enabled. |
| `project_id` | query | `string` | no | Space ID used to scope pages. |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `updated_recently` | query | `boolean` | no | Limit results to recently updated pages when enabled. |
