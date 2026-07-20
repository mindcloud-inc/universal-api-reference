# List Notes with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/notes`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [List Notes](https://superthread.com/docs/api-docs/notes/get-notes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of notes to return. |
| `cursor` | query | `string` | no | Cursor for pagination. |
| `team_id` | path | `string` | no | Workspace ID for the Superthread workspace. |
