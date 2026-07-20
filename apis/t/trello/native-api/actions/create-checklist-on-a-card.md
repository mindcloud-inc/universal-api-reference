# Create Checklist on a Card with Trello

Creates a checklist on a Trello card.

## Endpoint

- **Method:** `POST`
- **Path:** `cards/:id/checklists`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Create Checklist on a Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-checklists-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `name` | query | `string` | yes | Name for the checklist to create on card. |
