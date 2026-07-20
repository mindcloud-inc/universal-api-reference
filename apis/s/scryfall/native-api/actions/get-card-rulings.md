# Get Card Rulings with Scryfall

Retrieves card rulings from Scryfall by Scryfall ID.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/:id/rulings`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Card Rulings](https://scryfall.com/docs/api/rulings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Scryfall card UUID. |
