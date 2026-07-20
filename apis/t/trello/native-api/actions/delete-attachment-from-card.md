# Delete Attachment from Card with Trello

Deletes an attachment from a Trello card.

## Endpoint

- **Method:** `DELETE`
- **Path:** `cards/:id/attachments/:idAttachment`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Delete Attachment from Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-attachments-idattachment-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card identifier. |
| `idAttachment` | path | `string` | yes | Attachment identifier. |
