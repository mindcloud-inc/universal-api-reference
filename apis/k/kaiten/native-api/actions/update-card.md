# Update Card with Kaiten

Updates an existing card in Kaiten.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/cards/:cardId`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Update Card](https://developers.kaiten.ru/cards/{card_id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
| `title` | body | `string` | no | The card title. |
| `column_id` | body | `number` | no | The target column ID. |
| `lane_id` | body | `number` | no | The target lane ID. |
