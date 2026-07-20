# Get Note with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/notes/:note_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Get Note](https://superthread.com/docs/api-docs/notes/get-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note_id` | path | `string` | yes | Note ID to retrieve. |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
