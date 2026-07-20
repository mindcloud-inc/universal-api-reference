# Add Label to Card with Trello

Adds a label to a Trello card.

## Endpoint

- **Method:** `POST`
- **Path:** `cards/:id/idLabels`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Add Label to Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idlabels-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `value` | query | `string` | yes | Label ID to add to the card. |
