# Remove Member from Card with Kaiten

Removes a member from a Kaiten card.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/cards/:cardId/members/:id`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Remove Member from Card](https://developers.kaiten.ru/cards/{card_id}/members/{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `id` | path | `number` | yes | The Kaiten member user ID. |
