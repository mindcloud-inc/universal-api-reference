# Add Tag to Card with Kaiten

Adds a tag to a Kaiten card.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:cardId/tags`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Add Tag to Card](https://developers.kaiten.ru/cards/{card_id}/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `name` | body | `string` | yes | The tag name to attach to the card. |
