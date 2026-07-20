# Remove Comment with Kaiten

Deletes an existing comment from Kaiten.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/cards/:cardId/comments/:commentId`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Remove Comment](https://developers.kaiten.ru/cards/{card_id}/comments/{comment_id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `commentId` | path | `number` | yes | The Kaiten comment ID. |
