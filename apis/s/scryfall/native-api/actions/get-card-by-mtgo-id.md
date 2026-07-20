# Get Card By MTGO ID with Scryfall

Retrieves a card from Scryfall by MTGO ID.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/mtgo/:id`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Card By MTGO ID](https://scryfall.com/docs/api/cards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Magic Online card ID. |
