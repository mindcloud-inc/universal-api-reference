# Update Board with Trello

Updates an existing board in Trello.

## Endpoint

- **Method:** `PUT`
- **Path:** `boards/:id`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Update Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Board identifier. |
| `name` | query | `string` | no | Optional new board name. |
