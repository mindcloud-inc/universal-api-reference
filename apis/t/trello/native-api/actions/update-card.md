# Update Card with Trello

Updates an existing card in Trello.

## Endpoint

- **Method:** `PUT`
- **Path:** `cards/:id`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Update Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | query | `string` | no | Optional card description. |
| `id` | path | `string` | yes | Card identifier. |
| `idList` | query | `string` | no | Optional destination list ID for moving card. |
| `name` | query | `string` | no | Optional new card title. |
