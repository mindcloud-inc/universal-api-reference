# Add Attachment to Card with Trello

Adds an attachment to a Trello card.

## Endpoint

- **Method:** `POST`
- **Path:** `cards/:id/attachments`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Add Attachment to Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-attachments-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `url` | query | `string` | yes | Public URL to attach to the card. |
