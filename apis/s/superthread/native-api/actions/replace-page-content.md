# Replace Page Content with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/pages/:page_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Replace Page Content](https://superthread.com/docs/api-docs/pages/replace-a-page-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `page_id` | path | `string` | yes | Page ID to update. |
| `content` | body | `string` | yes | Full page content. |
