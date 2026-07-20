# Get MTGO Card Rulings with Scryfall

Retrieves card rulings from Scryfall by MTGO ID.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/mtgo/:id/rulings`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get MTGO Card Rulings](https://scryfall.com/docs/api/rulings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Magic Online card ID. |
