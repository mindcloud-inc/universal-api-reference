# Get Card By Name with Scryfall

Retrieves a card from Scryfall by name.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/named`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Card By Name](https://scryfall.com/docs/api/cards/named)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exact` | query | `string` | no |
| `fuzzy` | query | `string` | no |
| `set` | query | `list<string>` | no |
