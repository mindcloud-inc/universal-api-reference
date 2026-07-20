# Add Member to Card with Trello

Adds a member to a Trello card.

## Endpoint

- **Method:** `POST`
- **Path:** `cards/:id/idMembers`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Add Member to Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idmembers-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `value` | query | `string` | yes | Member ID to add to the card. |
