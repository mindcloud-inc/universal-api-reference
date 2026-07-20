# Get Actions on a Card with Trello

Retrieves actions on a card from Trello.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/:id/actions`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Get Actions on a Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-actions-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
