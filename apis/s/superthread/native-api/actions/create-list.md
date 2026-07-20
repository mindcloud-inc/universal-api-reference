# Create List with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/lists`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create List](https://superthread.com/docs/api-docs/boards/create-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `board_id` | body | `string` | yes | Board ID is a numerical string that identifies a Board. |
| `board_id` | body | `string` | yes | — |
| `title` | body | `string` | no | Title of the list to create. |
| `title` | body | `string` | yes | — |
