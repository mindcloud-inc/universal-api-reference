# Create Page with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/pages`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Page](https://superthread.com/docs/api-docs/pages/create-a-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `project_id` | body | `string` | yes | — |
| `title` | body | `string` | yes | — |
| `content` | body | `string` | no | — |
