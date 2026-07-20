# Update Member Role with Kaiten

Updates a card member role in Kaiten.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/cards/:cardId/members/:id`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Update Member Role](https://developers.kaiten.ru/cards/{card_id}/members/{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `id` | path | `number` | yes | The Kaiten member user ID. |
| `type` | body | `number` | yes | The numeric member role type. |
