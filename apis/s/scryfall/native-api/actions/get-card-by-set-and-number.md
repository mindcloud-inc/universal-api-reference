# Get Card By Set And Number with Scryfall

Retrieves a card from Scryfall by set and collector number.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/:code/:number`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Card By Set And Number](https://scryfall.com/docs/api/cards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Scryfall set code. |
| `number` | path | `string` | yes | Collector number within the set. |
