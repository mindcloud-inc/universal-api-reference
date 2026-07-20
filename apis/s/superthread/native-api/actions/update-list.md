# Update List with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/lists/:list_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update List](https://superthread.com/docs/api-docs/boards/update-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | no | List title. |
| `list_id` | path | `string` | yes | List ID to update. |
