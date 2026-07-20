# Retrieve Card Comments with Kaiten

Retrieves comments for a Kaiten card.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/:cardId/comments`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Retrieve Card Comments](https://developers.kaiten.ru/cards/{card_id}/comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
