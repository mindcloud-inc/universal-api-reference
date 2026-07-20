# Delete Card with Trello

Deletes an existing card from Trello.

## Endpoint

- **Method:** `DELETE`
- **Path:** `cards/:id`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Delete Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
