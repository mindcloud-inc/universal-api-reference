# Get Bulk Data with Scryfall

Retrieves a bulk data record from Scryfall by type.

## Endpoint

- **Method:** `GET`
- **Path:** `bulk-data/:type`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Bulk Data](https://scryfall.com/docs/api/bulk-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Bulk data type, such as oracle_cards, unique_artwork, default_cards, all_cards, or rulings. |
