# Add Comment to Card with Trello

Creates a comment on a Trello card.

## Endpoint

- **Method:** `POST`
- **Path:** `cards/:id/actions/comments`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Add Comment to Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-actions-comments-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `text` | query | `string` | yes | Comment text to add to the card. |
