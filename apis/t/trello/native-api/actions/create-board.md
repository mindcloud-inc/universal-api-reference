# Create Board with Trello

Creates a new board in Trello.

## Endpoint

- **Method:** `POST`
- **Path:** `boards`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Create Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name for the new board. |
