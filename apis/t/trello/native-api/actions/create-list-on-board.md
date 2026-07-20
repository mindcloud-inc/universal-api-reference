# Create List on Board with Trello

Creates a new list on a Trello board.

## Endpoint

- **Method:** `POST`
- **Path:** `boards/:id/lists`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Create List on Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-lists-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Board identifier. |
| `name` | query | `string` | yes | Name for the new list. |
