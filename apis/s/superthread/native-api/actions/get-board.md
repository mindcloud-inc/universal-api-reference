# Get Board with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/boards/:board_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Get Board](https://superthread.com/docs/api-docs/boards/get-a-board)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | yes | Board ID to retrieve. |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
