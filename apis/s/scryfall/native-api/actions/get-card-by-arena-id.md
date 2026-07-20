# Get Card By Arena ID with Scryfall

Retrieves a card from Scryfall by Arena ID.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/arena/:id`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Card By Arena ID](https://scryfall.com/docs/api/cards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Magic Arena card ID. |
