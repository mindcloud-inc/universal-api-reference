# Get Attachments on a Card with Trello

Retrieves attachments on a card from Trello.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/:id/attachments`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Get Attachments on a Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-attachments-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
