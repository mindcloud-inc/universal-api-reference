# Create Checklist with Trello

Creates a new checklist in Trello.

## Endpoint

- **Method:** `POST`
- **Path:** `checklists`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Create Checklist](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idCard` | query | `string` | yes | Card to attach the checklist to. |
| `name` | query | `string` | yes | Name of the checklist. |
