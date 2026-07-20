# Get Multiverse Card Rulings with Scryfall

Retrieves card rulings from Scryfall by Multiverse ID.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/multiverse/:id/rulings`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Multiverse Card Rulings](https://scryfall.com/docs/api/rulings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Wizards of the Coast Multiverse ID. |
