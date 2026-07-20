# Delete CheckItem from Checklist with Trello

Deletes a check item from a Trello checklist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `checklists/:id/checkItems/:idCheckItem`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Delete CheckItem from Checklist](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-id-checkitems-idcheckitem-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Checklist identifier. |
| `idCheckItem` | path | `string` | yes | Checklist item identifier. |
