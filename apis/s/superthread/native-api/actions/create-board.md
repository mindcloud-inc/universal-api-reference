# Create Board with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/boards`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Board](https://superthread.com/docs/api-docs/boards/create-a-board)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `project_id` | body | `string` | yes | Space ID to add the board to. |
| `title` | body | `string` | yes | Board title. |
