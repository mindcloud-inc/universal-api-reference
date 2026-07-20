# Archive Board with Trello

Archives an existing board in Trello.

## Endpoint

- **Method:** `PUT`
- **Path:** `boards/:id/closed`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Archive Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-closed-put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `value` | query | `boolean` | yes |
