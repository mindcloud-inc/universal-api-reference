# Update Comment with Kaiten

Updates an existing comment in Kaiten.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/cards/:cardId/comments/:commentId`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Update Comment](https://developers.kaiten.ru/cards/{card_id}/comments/{comment_id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `commentId` | path | `number` | yes | The Kaiten comment ID. |
| `text` | body | `string` | yes | The comment text. |
