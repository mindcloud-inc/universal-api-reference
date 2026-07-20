# Archive List with Trello

Archives an existing list in Trello.

## Endpoint

- **Method:** `PUT`
- **Path:** `lists/:id/closed`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Archive List](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-closed-put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `value` | query | `boolean` | yes |
