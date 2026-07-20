# Add Comment with Kaiten

Creates a comment on a Kaiten card.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:cardId/comments`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Add Comment](https://developers.kaiten.ru/cards/{card_id}/comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `text` | body | `string` | yes | The comment text. |
