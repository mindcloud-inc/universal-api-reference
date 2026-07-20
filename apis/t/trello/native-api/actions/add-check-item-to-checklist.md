# Add CheckItem to Checklist with Trello

Creates a check item in a Trello checklist.

## Endpoint

- **Method:** `POST`
- **Path:** `checklists/:id/checkItems`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Add CheckItem to Checklist](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-id-checkitems-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Checklist identifier. |
| `name` | query | `string` | yes | Checklist item name. |
