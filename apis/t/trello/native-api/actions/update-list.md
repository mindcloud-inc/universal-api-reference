# Update List with Trello

Updates an existing list in Trello.

## Endpoint

- **Method:** `PUT`
- **Path:** `lists/:id`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Update List](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | List identifier. |
| `name` | query | `string` | no | Optional new list name. |
