# Remove Member from Card with Trello

Removes a member from a Trello card.

## Endpoint

- **Method:** `DELETE`
- **Path:** `cards/:id/idMembers/:idMember`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Remove Member from Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idmembers-idmember-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `idMember` | path | `string` | yes | Member identifier. |
