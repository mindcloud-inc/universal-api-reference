# Retrieve List of Card Tags with Kaiten

Retrieves tags for a Kaiten card.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/:cardId/tags`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Retrieve List of Card Tags](https://developers.kaiten.ru/cards/{card_id}/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `number` | yes | The Kaiten card ID. |
