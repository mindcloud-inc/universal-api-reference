# Remove Tag from Card with Kaiten

Removes a tag from a Kaiten card.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/cards/:cardId/tags/:tagId`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Remove Tag from Card](https://developers.kaiten.ru/cards/{card_id}/tags/{tag_id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `tagId` | path | `number` | yes | The Kaiten tag ID. |
