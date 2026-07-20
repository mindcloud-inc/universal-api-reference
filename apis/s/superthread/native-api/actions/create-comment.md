# Create Comment with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/comments`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Comment](https://superthread.com/docs/api-docs/comments/create-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `content` | body | `string` | yes | — |
| `page_id` | body | `string` | no | — |
| `card_id` | body | `string` | no | — |
