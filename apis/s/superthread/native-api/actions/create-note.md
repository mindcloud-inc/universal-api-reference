# Create Note with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/notes`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Note](https://superthread.com/docs/api-docs/notes/create-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | yes | — |
| `content` | body | `string` | yes | — |
