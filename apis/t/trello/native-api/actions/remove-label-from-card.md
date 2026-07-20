# Remove Label from Card with Trello

Removes a label from a Trello card.

## Endpoint

- **Method:** `DELETE`
- **Path:** `cards/:id/idLabels/:idLabel`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Remove Label from Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idlabels-idlabel-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `idLabel` | path | `string` | yes | Label identifier. |
