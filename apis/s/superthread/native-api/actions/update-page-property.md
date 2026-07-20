# Update Page Property with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/pages/:page_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update Page Property](https://superthread.com/docs/api-docs/pages/update-a-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | no | Page title. |
| `page_id` | path | `string` | yes | Page ID to update. |
