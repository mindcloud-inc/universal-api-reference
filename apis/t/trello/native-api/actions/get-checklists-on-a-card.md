# Get Checklists on a Card with Trello

Retrieves checklists on a card from Trello.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/:id/checklists`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Get Checklists on a Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-checklists-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
