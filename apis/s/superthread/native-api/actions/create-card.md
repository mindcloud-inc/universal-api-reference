# Create Card with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/cards`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Card](https://superthread.com/docs/api-docs/cards/create-a-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | yes | — |
| `list_id` | body | `string` | yes | — |
| `board_id` | body | `string` | yes | — |
