# Add Member to Card with Kaiten

Adds a member to a Kaiten card.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:cardId/members`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Add Member to Card](https://developers.kaiten.ru/cards/{card_id}/members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `user_id` | body | `number` | yes | The Kaiten user ID to add to the card. |
| `type` | body | `number` | yes | The numeric member role type. |
