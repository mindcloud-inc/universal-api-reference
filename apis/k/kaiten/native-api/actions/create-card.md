# Create Card with Kaiten

Creates a card in Kaiten.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Create Card](https://developers.kaiten.ru/cards/create-new-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The card title. |
| `board_id` | body | `number` | yes | The Kaiten board ID. |
| `column_id` | body | `number` | no | The target column ID. |
| `lane_id` | body | `number` | no | The target lane ID. |
