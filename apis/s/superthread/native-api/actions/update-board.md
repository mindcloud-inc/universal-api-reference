# Update Board with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/boards/:board_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update Board](https://superthread.com/docs/api-docs/boards/update-a-board)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | no | Board title. |
| `board_id` | path | `string` | yes | Board ID to update. |
